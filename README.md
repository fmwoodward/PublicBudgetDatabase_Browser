# PublicBudgetDatabase_Browser
## Browsing Federal Budget 
The U.S. federal government website [GovInfo](https://www.govinfo.gov/app/collection/budget/) provides a wealth of information about the U.S. Economy, the Federal budget, the yearly President's budget request, and OMB's assessment of future economic conditions.
### Data
This project stacks the budget positions between 2000 and 2019 from the Public Budget Database in a single xlsx workbook (*OMB-PBDB_FY00-FY19.xlsx*) creating a dataset that allows for the comparision of Plans and projected spending to what was actually appropriated.  This project looks at both manditory and discretionary budget authority across the whole of government.
### Processing
The data are mannually packed into the xlsx workbook *OMB-PBDB_FY00-FY19.xlsx* with each tab corresponding to a fiscal year budget request.  

The aggreate file is then manipulated using Python 2.7 scripts in a Jupyter Notebook working environment relying on pandas for manipulation and matplotlib or plotly for visualiztion.  The data for DoD are extracted and output to the file *OMB-PBDB-DoD.xlsx*.

GDP deflator, the GDP (Chained) Price Index, found in the President's Budget submission, History [Table 10.1](https://www.govinfo.gov/app/details/BUDGET-2019-TAB/BUDGET-2019-TAB-11-1
) is used to remove the effects of inflation, converting nominal dollars into real dollars.
