# 📊 DAX Table Functions -- Interview Notes

## 🔹 Definition

Table functions in DAX return a table instead of a single value.\
They are mainly used in advanced calculations with SUMX, CALCULATE, and
virtual tables.

------------------------------------------------------------------------

# 1️⃣ SUMMARIZE()

### Definition:

Creates a summary table grouped by specified columns (Similar to SQL
GROUP BY).

### Syntax:

SUMMARIZE(Table, GroupBy_Column1, "NewColumn", Expression)

### Example:

SUMMARIZE( Sales, Sales\[Region\], "Total Sales",
SUM(Sales\[SalesAmount\]) )

### Interview Points:

-   Used for grouping
-   Returns a table
-   Can create calculated columns inside

------------------------------------------------------------------------

# 2️⃣ ADDCOLUMNS()

### Definition:

Adds new calculated columns to an existing table.

### Syntax:

ADDCOLUMNS(Table, "NewColumn", Expression)

### Example:

ADDCOLUMNS( Sales, "Tax", Sales\[SalesAmount\] \* 0.10 )

### Interview Points:

-   Does not modify original table
-   Creates virtual table
-   Often used with SUMX

------------------------------------------------------------------------

# 3️⃣ SELECTCOLUMNS()

### Definition:

Creates a new table by selecting specific columns.

### Syntax:

SELECTCOLUMNS(Table, "NewName", Table\[Column\])

### Example:

SELECTCOLUMNS( Products, "Product Name", Products\[ProductName\],
"Price", Products\[Price\] )

### Interview Points:

-   Similar to SELECT in SQL
-   Allows renaming columns
-   Returns only selected columns

------------------------------------------------------------------------

# 4️⃣ VALUES()

### Definition:

Returns distinct values from a column as a table.

### Syntax:

VALUES(Table\[Column\])

### Example:

VALUES(Sales\[CustomerID\])

### Interview Points:

-   Respects filter context
-   Can return blank row if relationship issue exists

------------------------------------------------------------------------

# 5️⃣ DISTINCT()

### Definition:

Returns unique values from a column.

### Syntax:

DISTINCT(Table\[Column\])

### Example:

DISTINCT(Sales\[Product\])

### Interview Points:

-   Returns unique values only
-   Does not add blank row like VALUES

------------------------------------------------------------------------

# 🔥 VALUES vs DISTINCT

  VALUES                    DISTINCT
  ------------------------- -----------------------------
  Respects filter context   Returns unique values
  Can return blank row      Does not return blank row
  Used in advanced DAX      Used for simple unique list

------------------------------------------------------------------------

# 🎯 Common Interview Questions & Answers

### Q1: Difference between SUMMARIZE and ADDCOLUMNS?

SUMMARIZE groups data.\
ADDCOLUMNS adds calculated columns to an existing table.

### Q2: Difference between SELECTCOLUMNS and ADDCOLUMNS?

SELECTCOLUMNS selects specific columns only.\
ADDCOLUMNS keeps all existing columns and adds new ones.

### Q3: Difference between VALUES and DISTINCT?

VALUES may return a blank row due to relationship issues.\
DISTINCT only returns unique values.

### Q4: When are table functions used?

Table functions are used in advanced DAX calculations, especially with
iterator functions like SUMX and in virtual tables.

------------------------------------------------------------------------

# 🔹 Short Interview Summary

"Table functions in DAX return tables instead of scalar values.
SUMMARIZE groups data, ADDCOLUMNS adds calculated columns, SELECTCOLUMNS
selects specific columns, VALUES returns distinct values respecting
filter context, and DISTINCT returns unique values. They are essential
for advanced DAX modeling."
