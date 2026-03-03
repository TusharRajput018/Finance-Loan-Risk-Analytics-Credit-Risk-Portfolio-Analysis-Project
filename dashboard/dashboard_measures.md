## Total Customer
Total Customer = COUNTA(Dim_Customer[Customer_id])

## fact
fact = Fact_Finance[Avg.Prop_Value]

## Loan Growth YoY %
Loan Growth YoY % = 
VAR CurrentYear = MAX('Dim_Calender'[Year])
VAR CurrentAmount = 
    CALCULATE(
        SUM(Fact_Finance[loan_amount]), 
        'Dim_Calender'[Year] = CurrentYear
    )
VAR PreviousAmount = 
    CALCULATE(
        SUM(Fact_Finance[loan_amount]), 
        'Dim_Calender'[Year] = CurrentYear - 1
    )
RETURN
    DIVIDE(CurrentAmount - PreviousAmount, PreviousAmount, 0)

## Avg LTV Per
Avg LTV Per = AVERAGE(Fact_Finance[LTV %])

## Avg.Prop_Value
Avg.Prop_Value = AVERAGE(Fact_Finance[property_value])

## Income Band
Income Band = 
SWITCH(
    TRUE(),
    Fact_Finance[income] < 2500, "Low",
    'Fact_Finance'[income] < 5000, "Middle",
    'Fact_Finance'[income] < 10000, "Upper Middle",
    "High"
)

## Calculated Values 

## LTV %
LTV % = 
DIVIDE(
    'Fact_Finance'[LTV],
    100
)

## LTV Band
LTV Band = 
SWITCH(
    TRUE(),
    'Fact_Finance'[LTV %] < 60, "< 60%",
    'Fact_Finance'[LTV %] < 80, "60–80%",
    'Fact_Finance'[LTV %] < 90, "80–90%",
    "90%+"
)
