# PublicBudgetDatabase_Browser
## Browsing Federal Budget 
The U.S. federal government website [GovInfo](https://www.govinfo.gov/app/collection/budget/) provides a wealth of information about the U.S. Economy, the Federal budget, the yearly President's budget request, and OMB's assessment of future economic conditions.
### Data
This project stacks the budget positions between 2000 and 2019 from the Public Budget Database in a single xlsx workbook (*OMB-PBDB_FY00-FY19.xlsx*) creating a dataset that allows for the comparison of planned spending to actual appropriations.  This project looks at both mandatory and discretionary budget authority across the whole of government.

A GDP deflator, the GDP (Chained) Price Index, found in the President's Budget submission, History [Table 10.1](https://www.govinfo.gov/app/details/BUDGET-2019-TAB/BUDGET-2019-TAB-11-1
) is used to remove the effects of inflation, converting nominal dollars into real dollars.

An alternative to OMB’s economic assumptions in the President's Budget can be found in the most current 10-year economic projection accompanying [CBO’s Budget Outlook](https://www.cbo.gov/about/products/budget-economic-data#4).  This file also includes a projection of other useful deflators such as the employment cost index (ECI).  


### Processing
The data are manually packed into the xlsx workbook *OMB-PBDB_FY00-FY19.xlsx* with each tab corresponding to a fiscal year budget request.  

The data are manipulated using a Jupyter Notebook computational environment environment and the [Python 2.7 kernel](https://www.python.org/download/releases/2.7/) with [Pandas](https://pandas.pydata.org/) software library for data manipulation and [Matplotlib](https://matplotlib.org/) or [Plotly](https://plot.ly/) software libraries for visualization **OMB_PublicBudget_DB_Browser.ipynb**.  An example data set for DoD extracted from the master file *OMB-PBDB_FY00-FY19.xlsx* is found in the file *OMB-PBDB-DoD.xlsx*.

## Resource Planning Trajectories
DoD data in the file *OMB-PBDB-DoD.xlsx* is processed using the Jupyter Notebook **OMB_Trajectories** to compare Planned, Budgeted, and Enacted funding.  To compare planned or required base budget funding to enacted base budget funding, the nonbase funding is removed from total enacted funding using data found in Table 2.1 of the DoD National Defense Budget Estimates [Green Book](https://comptroller.defense.gov/Budget-Materials/).

# Results!
## There is a hole in the data set!  Data for the out-years of the FYDP are missing between 2006 and 2009 making the dataset unusable for Projected/Enacted analysis.
It is still a very detailed set of data showing spending across the federal government 
