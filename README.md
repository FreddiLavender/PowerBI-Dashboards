# PowerBI Learning # 

My PowerBI journey began through LinkedIn courses, understanding the basics of Dashboarding, Data Modelling and Visualisation work. 

# Dashboard Creations #

This Repo will be dedicated to showcase dashboards that I have created in my own time. 

# DAX Code #

Some example DAX code:

TOTAL SALES = 
CALCULATE(SUM('Sheet1'[ Sales]), ALLSELECTED('Sheet1'[Year]))

PROFIT % DIFFERENCE IN 2013 = 
VAR __BASELINE_VALUE = CALCULATE(SUM('financials'[Profit]), 'financials'[Year] IN { 2013 })
VAR __MEASURE_VALUE = SUM('financials'[Profit])
RETURN
	IF(
		NOT ISBLANK(__MEASURE_VALUE),
		DIVIDE(__MEASURE_VALUE - __BASELINE_VALUE, __BASELINE_VALUE)
	)

