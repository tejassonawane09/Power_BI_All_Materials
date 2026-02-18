# DAX Time Intelligence Functions 
## Important Requirement

To use Time Intelligence functions: - Proper Date Table - Continuous
date column - Mark as Date Table in Power BI - Relationship between Date
table and Fact table

------------------------------------------------------------------------

# 1️⃣ TOTALYTD()

## Definition

Calculates cumulative total from the beginning of the year until the
selected date.

## Syntax

``` dax
TOTALYTD(Expression, DateColumn, [Filter])
```

## Example

``` dax
Sales YTD =
TOTALYTD(
    SUM(Sales[SalesAmount]),
    'Date'[Date]
)
```

## Interview Points

-   Used for Year-To-Date calculations
-   Automatically starts from Jan 1
-   Requires proper Date table

------------------------------------------------------------------------

# 2️⃣ SAMEPERIODLASTYEAR()

## Definition

Returns values for the same period in the previous year.

## Syntax

``` dax
CALCULATE(Expression, SAMEPERIODLASTYEAR(DateColumn))
```

## Example

``` dax
Sales Last Year =
CALCULATE(
    SUM(Sales[SalesAmount]),
    SAMEPERIODLASTYEAR('Date'[Date])
)
```

## Interview Points

-   Used for YoY comparison
-   Shifts exactly one year back
-   Requires Date table

------------------------------------------------------------------------

# 3️⃣ DATEADD()

## Definition

Shifts date context forward or backward by specified interval.

## Syntax

``` dax
DATEADD(DateColumn, Number, Interval)
```

## Example

``` dax
Previous Month Sales =
CALCULATE(
    SUM(Sales[SalesAmount]),
    DATEADD('Date'[Date], -1, MONTH)
)
```

## Interview Points

-   Flexible (day, month, quarter, year)
-   Used for MoM, QoQ, YoY analysis

------------------------------------------------------------------------

# 4️⃣ DATESYTD()

## Definition

Returns a table of dates from start of year to current date.

## Syntax

``` dax
CALCULATE(Expression, DATESYTD(DateColumn))
```

## Example

``` dax
Sales YTD =
CALCULATE(
    SUM(Sales[SalesAmount]),
    DATESYTD('Date'[Date])
)
```

## Interview Difference

-   TOTALYTD returns value
-   DATESYTD returns date table

------------------------------------------------------------------------

# 5️⃣ PARALLELPERIOD()

## Definition

Returns dates shifted by full period (month/quarter/year).

## Syntax

``` dax
PARALLELPERIOD(DateColumn, Number, Interval)
```

## Example

``` dax
Previous Year Sales =
CALCULATE(
    SUM(Sales[SalesAmount]),
    PARALLELPERIOD('Date'[Date], -1, YEAR)
)
```

## Interview Points

-   Shifts full period
-   Used for period comparison

------------------------------------------------------------------------

# Common Interview Questions

## 1️⃣ What is YTD?

Cumulative total from start of year till selected date.

## 2️⃣ Difference between TOTALYTD and DATESYTD?

TOTALYTD returns value.\
DATESYTD returns date table.

## 3️⃣ Difference between DATEADD and SAMEPERIODLASTYEAR?

SAMEPERIODLASTYEAR shifts exactly 1 year.\
DATEADD can shift any number of months/years/days.

## 4️⃣ Why is Date Table required?

Time Intelligence functions require continuous date column to work
properly.

## 5️⃣ How to calculate YoY Growth %?

``` dax
YoY Growth % =
DIVIDE(
    [Total Sales] - [Sales Last Year],
    [Sales Last Year]
)
```

------------------------------------------------------------------------

# Final Interview Summary

Time Intelligence functions in DAX are used for date-based calculations
like YTD, YoY, MoM.\
TOTALYTD calculates cumulative yearly sales.\
SAMEPERIODLASTYEAR compares previous year.\
DATEADD shifts date context.\
DATESYTD returns YTD date table.\
PARALLELPERIOD shifts full periods.
