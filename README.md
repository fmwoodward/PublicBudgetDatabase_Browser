# PublicBudgetDatabase_Browser
## Browsing Federal Budget 
The U.S. federal government website [GovInfo](https://www.govinfo.gov/app/collection/budget/) provides a wealth of information about the U.S. Economy, the Federal budget, the yearly President's budget request, and OMB's assessment of future economic conditions.
### Data
This project stacks the budget positions between 2000 and 2019 from the Public Budget Database in a single xlsx workbook (*OMB-PBDB_FY00-FY19.xlsx*) creating a dataset that allows for the comparision of planned spending to actual appropriations.  This project looks at both manditory and discretionary budget authority across the whole of government.

A GDP [deflator](), the GDP (Chained) Price Index, found in the President's Budget submission, History [Table 10.1](https://www.govinfo.gov/app/details/BUDGET-2019-TAB/BUDGET-2019-TAB-11-1
) is used to remove the effects of inflation, converting nominal dollars into real dollars.

### Processing
The data are mannually packed into the xlsx workbook *OMB-PBDB_FY00-FY19.xlsx* with each tab corresponding to a fiscal year budget request.  

The data are manipulated using a Jupyter Notebook computational environment environment and the [Python 2.7 kernal](https://www.python.org/download/releases/2.7/) with [Pandas](https://pandas.pydata.org/) software library for data manipulation and [Matplotlib](https://matplotlib.org/) or [Plotly](https://plot.ly/) software libraries for visualiztion [OMB_PublicBUdge_tDB_Browser.ipynb](PublicBudgetDatabase_Browser/OMB_PublicBudget_DB_Browser.ipynb).  An example data set for DoD extracted from the master file *OMB-PBDB_FY00-FY19.xlsx* is found in the file *OMB-PBDB-DoD.xlsx*.
