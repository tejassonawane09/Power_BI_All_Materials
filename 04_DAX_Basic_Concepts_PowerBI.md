
# DAX – Basic Concepts 


## 1. Measures

### What it is
A Measure is a calculation created for analysis that changes based on filters.

### Key Points
- Measures are dynamic.
- They recalculate when slicers or filters change.
- Used for KPIs and dashboard calculations.

---

## 2. Calculated Columns

### What it is
A Calculated Column is a new column added to a table using DAX.

### Key Points
- Calculated row by row.
- Static after calculation.
- Used for classification or row-level logic.

---

## 3. Aggregation Functions

### What they are
Functions that combine many values into one value.

### Common Examples
- SUM
- AVERAGE
- COUNT

### Purpose
Used to calculate totals and summary metrics.

---

## 4. Logical Functions

### What they are
Functions that apply conditions (if–else logic).

### Common Examples
- IF
- SWITCH

### Purpose
Used to classify or label data based on business rules.

---

## 5. Filter Functions

### What they are
Functions that control which data is included in a calculation.

### Common Examples
- FILTER
- ALL

### Purpose
Used to calculate values under specific conditions.

---

## 6. Iterator Functions

### What they are
Functions that evaluate data row by row and then aggregate results.

### Common Examples
- SUMX
- AVERAGEX

### Purpose
Used when calculations require row-level logic before aggregation.

---

## 7. Time Intelligence Functions

### What they are
Functions used to analyze data across time periods.

### Examples of Usage
- Year-to-Date
- Month-to-Date
- Year-over-Year comparison

### Requirement
Requires a proper Date Table marked as Date Table.

---

## 8. CALCULATE

### What it is
The most important DAX function.

### What it does
Evaluates a measure under specific filter conditions.

### Purpose
Used to modify filter context.

---

## 9. FILTER

### What it is
Returns a filtered table based on conditions.

### Purpose
Used for row-level filtering inside calculations.

---

## 10. ALL

### What it is
Removes existing filters from a column or table.

### Purpose
Used to calculate overall totals ignoring slicers.

---

## 11. SUM

### What it is
Adds all numeric values in a column.

### Purpose
Used to calculate totals.

---

## 12. AVERAGE

### What it is
Calculates the mean value of a column.

### Purpose
Used to understand typical performance.

---

## 13. COUNT

### What it is
Counts the number of non-empty values in a column.

### Purpose
Used to count records or transactions.

---

## 14. DIVIDE

### What it is
Performs safe division.

### Purpose
Prevents division-by-zero errors.
Commonly used for profit margin and growth percentage.

---

## One-line Summary

DAX enables creation of dynamic calculations, logical rules, filter-based analysis, and time-based performance tracking in Power BI.


