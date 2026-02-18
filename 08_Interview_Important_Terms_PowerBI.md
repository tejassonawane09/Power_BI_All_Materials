
# Interview-Important Terms 


# 1. Measures vs Calculated Columns

## Measures

### What It Is
A Measure is a dynamic calculation that changes based on filters applied in the report.

### Key Characteristics
- Calculated during report usage
- Not stored in the data model
- Depends on filter context
- Used mainly for KPIs

### Example
If Region = North is selected, Total Sales measure recalculates automatically for North.

### Interview Answer
Measures are dynamic calculations evaluated based on filter context and are typically used for aggregated metrics like sales or profit.

---

## Calculated Columns

### What It Is
A Calculated Column is a new column created using DAX that is calculated row by row.

### Key Characteristics
- Calculated during data load
- Stored in the model
- Does not change based on slicers
- Used for row-level classification

### Example
Profit = Sales − Cost calculated for each row.

### Interview Answer
Calculated columns are static row-level computations stored in the data model and do not change based on report filters.

---

# 2. Import vs DirectQuery

## Import Mode

### What It Is
Data is loaded and stored inside Power BI.

### Advantages
- Fast performance
- Works offline
- Suitable for small to medium datasets

### Disadvantages
- Requires refresh to update data
- Uses memory

### Interview Answer
Import mode loads data into Power BI for faster performance and offline analysis.

---

## DirectQuery Mode

### What It Is
Data remains in the source database and Power BI queries it live.

### Advantages
- Real-time data
- Suitable for very large datasets

### Disadvantages
- Slower performance
- Depends on database speed

### Interview Answer
DirectQuery retrieves data in real-time from the source system without storing it locally in Power BI.

---

# 3. Filter Context

## What It Is
Filter Context refers to the filters applied to a calculation.

### Example
If Year = 2023 and Region = North are selected, Total Sales calculates only for those filters.

### Why It Matters
Measures change based on filter context.

### Interview Answer
Filter Context is the set of filters that determine how a measure is evaluated in a report.

---

# 4. Row Context

## What It Is
Row Context refers to calculations performed one row at a time.

### Where It Exists
- Calculated Columns
- Iterator functions such as SUMX

### Example
Profit = Sales − Cost calculated separately for each row.

### Interview Answer
Row Context refers to row-by-row evaluation of expressions in calculated columns or iterator functions.

---

# 5. Business Logic

## What It Is
Business Logic defines rules and conditions used in calculations.

### Example
- Revenue excludes returns
- Profit excludes tax
- Margin calculated before discount

### Why It Matters
Incorrect business logic leads to misleading KPIs.

### Interview Answer
Business Logic represents calculation rules aligned with actual business processes and reporting standards.

---

# 6. Data Validation

## What It Is
Data Validation ensures data accuracy and consistency before analysis.

### What To Check
- Missing values
- Duplicate records
- Incorrect relationships
- Mismatched totals

### Why It Matters
Wrong data leads to wrong decisions.

### Interview Answer
Data Validation ensures datasets are clean, accurate, and reliable before being used for reporting.

---

# Final Summary

Measures → Dynamic calculations  
Calculated Columns → Row-level stored values  
Import → Stored data for faster performance  
DirectQuery → Live database connection  
Filter Context → Filters affecting measures  
Row Context → Row-by-row calculation  
Business Logic → Reporting rules  
Data Validation → Accuracy assurance  

