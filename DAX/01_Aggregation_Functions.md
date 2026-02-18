
# 📊 DAX Aggregation Functions – Power BI 

## 🔹 Definition
Aggregation functions in DAX are used to perform mathematical calculations on a column of data and return a single summarized value.  
They are mainly used in **Measures**.

---

# 1️⃣ SUM()

### ✅ Definition
Returns the total (addition) of all numeric values in a column.

### ✅ Syntax
```DAX
SUM(TableName[ColumnName])
```

### ✅ Real Example
```DAX
Total Sales = SUM(Sales[SalesAmount])
```
👉 Adds all SalesAmount values.

---

# 2️⃣ AVERAGE()

### ✅ Definition
Returns the average (mean) of numeric values in a column.

### ✅ Syntax
```DAX
AVERAGE(TableName[ColumnName])
```

### ✅ Real Example
```DAX
Average Sales = AVERAGE(Sales[SalesAmount])
```

---

# 3️⃣ MIN()

### ✅ Definition
Returns the smallest value in a column.

### ✅ Syntax
```DAX
MIN(TableName[ColumnName])
```

### ✅ Real Example
```DAX
Minimum Sales = MIN(Sales[SalesAmount])
```

---

# 4️⃣ MAX()

### ✅ Definition
Returns the largest value in a column.

### ✅ Syntax
```DAX
MAX(TableName[ColumnName])
```

### ✅ Real Example
```DAX
Maximum Sales = MAX(Sales[SalesAmount])
```

---

# 5️⃣ COUNT()

### ✅ Definition
Counts the number of non-blank numeric values in a column.

### ✅ Syntax
```DAX
COUNT(TableName[ColumnName])
```

### ✅ Important
- Counts only numbers  
- Ignores blank values  
- Does NOT count text  

---

# 6️⃣ DISTINCTCOUNT()

### ✅ Definition
Counts the number of unique values in a column.

### ✅ Syntax
```DAX
DISTINCTCOUNT(TableName[ColumnName])
```

### ✅ Real Example
```DAX
Total Customers = DISTINCTCOUNT(Sales[CustomerID])
```

---

# 🔥 Differences (Interview Table)

| Function | Purpose | Works On |
|----------|----------|----------|
| SUM | Adds values | Numbers |
| AVERAGE | Mean value | Numbers |
| MIN | Smallest value | Number/Date |
| MAX | Largest value | Number/Date |
| COUNT | Counts numeric rows | Numbers only |
| DISTINCTCOUNT | Counts unique values | Any column |

---

# 🎯 Common Interview Questions

### Q1: What are aggregation functions in DAX?
Aggregation functions summarize data and return a single value like total, average, minimum, maximum, or count.

### Q2: What is the difference between COUNT and DISTINCTCOUNT?
COUNT counts all numeric rows.  
DISTINCTCOUNT counts only unique values.

### Q3: Can SUM work on a text column?
No. SUM works only on numeric columns.

### Q4: Where are aggregation functions mainly used?
They are mainly used inside Measures to create KPIs and business reports.

### Q5: Does AVERAGE ignore blank values?
Yes, AVERAGE ignores blank values.

---

# 🎯Summary Answer

Aggregation functions in DAX are used to summarize numeric data.  
SUM calculates totals, AVERAGE finds mean, MIN and MAX return extreme values, COUNT counts numeric records, and DISTINCTCOUNT counts unique values.  
They are mainly used in measures for business reporting.
