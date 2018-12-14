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

# The Relationship Between Planned and Enacted Funding

## DoD Resource Management:  Planning, Programing, Budget, Execution

DoD builds budget request as part of an integrated Planning, Programming, Budgeting, and Execution process.  

The request balance priorities to create a budget that meets current operational needs while planning to spend according to a multi-year program that will achieve longer-term strategic goals.

This process prioritizes current funding requirements using a mix of recent experiences and anticipated future needs to create a current budget.


### Categories of Defense Funding:  Enacted, Estimated, Requested
Funding in this analysis is labeled relative to the year of the President's Budget (PB) request with the following convention:  **BY-2, BY-1, BY+0, BY+1, BY+2, BY+3, BY+4**.  In this case, **BY** stands for Budget Year, and represents the fiscal year that funding is being requested for. 

In DoD's budget documentation data are typically represented in three year increments as follows: **BY-2** is the *enacted* funding, **BY-1** is an *estimate* of the current level of funding, **BY+0** is President's Budget (PB) *request*.  The *Enacted* funding for a particular fiscal year is the actual value of defense spending to which planned funding levels are compared.  In budget documentation funding in years less than BY-1 are consider enacted funding.   

For example, the 2020 PB will show FY2018, FY2019, and FY2020 funding positions.  FY2020 is labeled the *requested* amount.  FY2019 is labeled the *estimated* amount (budget in progress).  FY2018 is labeled the *actual* or *enacted* amount.  The amount is assumed to reflect the total appropriated funding for that year -- including recessions and transfers) for that fiscal year.  It is expected that this value will not change over time.<sup>[1]</sup>

The PB request will include a funding plan that typically spans five year, known as the Future Years Defense Program (FYDP).  The first year of that plan, **BY+0**, is the budget request with the following four years labeled **BY+1 ... BY+4**.

### Defense Funding Data
Comparison are made at the Public Law title level.  All data are from the National Defense Budget Estimates (Green Book) for fiscal years 2001 to 2019.<sup>[2]</sup>

- The program data for each FYDP are from Table 6-7.
- Enacted total funding data come from Table 6-8 in the Green Book, for all years prior to 2018.
- Enacted base-budget funding data are computed by subtracting nonbase funding data in Table 2.1 of the Green Book from [total] funding data in Table 6-8.
- FYDP data in Table 6-7 do not include nonbase funding.<sup>[3]</sup> 

Data are converted from nominal to real dollars using the CBO/Macroeconomics Analysis Division's Wiki, pgdp deflator version 161206e.

<sup><sup>[1]</sup>per private communication with OSD-C, Program and Financial Control (P&FC) directorate, the following terms mean: **Requested**, the amount submitted to Congress in the President's Budget for a particular account; **Enacted**, the amount appropriated by Congress for a particular account which may include adjustments for subsequent rescissions; **Actuals**, the amount executed for that account in the given Prior Year, based on Treasury certified accounting data, which may include adjustments for reprogramming actions.</sup>

<sup><sup>[2]</sup>Green Book data are found at [OSD Comptroller's website](http://comptroller.defense.gov/BudgetMaterials.aspx), tabular data is provided as a PDF and xls workbooks.  All data used from the Green Book are **Budget Authority (Discretionary and Mandatory)**, Millions of dollars at current year or nominal (not adjusted for inflation) monetary levels.</sup>

<sup><sup>[3]</sup>The exception is fiscal year 2019 of the 2019 President's Budget request which includes nonbase funding in the 2019 column of Table 6-8.
