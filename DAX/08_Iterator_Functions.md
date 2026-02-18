# 📘 DAX Iterator Functions (X Functions) -- Interview Notes

## 🔹 Definition

Iterator functions in DAX iterate (loop) through each row of a table,
evaluate an expression for each row, and then return an aggregated
result.

👉 Normal functions work on a column.\
👉 X functions work on an expression row by row.

------------------------------------------------------------------------

# 1️⃣ SUMX()

## ✅ Definition

Calculates the sum of an expression evaluated for each row.

## ✅ Syntax

``` dax
SUMX(Table, Expression)
```

## ✅ Example

``` dax
Total Revenue =
SUMX(
    Sales,
    Sales[Quantity] * Sales[Price]
)
```

------------------------------------------------------------------------

# 2️⃣ AVERAGEX()

## ✅ Definition

Calculates the average of an expression evaluated row by row.

## ✅ Syntax

``` dax
AVERAGEX(Table, Expression)
```

## ✅ Example

``` dax
Average Revenue =
AVERAGEX(
    Sales,
    Sales[Quantity] * Sales[Price]
)
```

------------------------------------------------------------------------

# 3️⃣ COUNTX()

## ✅ Definition

Counts rows where the evaluated expression is not blank.

## ✅ Syntax

``` dax
COUNTX(Table, Expression)
```

## ✅ Example

``` dax
Valid Orders =
COUNTX(
    Sales,
    Sales[Quantity] * Sales[Price]
)
```

------------------------------------------------------------------------

# 4️⃣ MAXX()

## ✅ Definition

Returns the maximum value of an expression evaluated row by row.

## ✅ Syntax

``` dax
MAXX(Table, Expression)
```

## ✅ Example

``` dax
Max Revenue =
MAXX(
    Sales,
    Sales[Quantity] * Sales[Price]
)
```

------------------------------------------------------------------------

# 5️⃣ MINX()

## ✅ Definition

Returns the minimum value of an expression evaluated row by row.

## ✅ Syntax

``` dax
MINX(Table, Expression)
```

## ✅ Example

``` dax
Min Revenue =
MINX(
    Sales,
    Sales[Quantity] * Sales[Price]
)
```

------------------------------------------------------------------------

# 🔥 Normal vs X Functions

  Normal Function        X Function
  ---------------------- ---------------------------
  Works on column        Works on expression
  SUM(Sales\[Amount\])   SUMX(Sales, Qty \* Price)
  No row iteration       Row-by-row iteration

------------------------------------------------------------------------

# 🎯 Common Interview Questions

### Q1: Difference between SUM and SUMX?

SUM works only on a column.\
SUMX works on an expression row by row.

### Q2: When do we use SUMX?

When calculation requires multiple columns (e.g., Quantity × Price).

### Q3: What is Row Context?

Row context means DAX evaluates an expression for each row
individually.\
Iterator functions automatically create row context.

### Q4: Which iterator function is most used in real projects?

SUMX is most commonly used for revenue and profit calculations.

------------------------------------------------------------------------

# ✅ Final Interview Answer (Short Version)

Iterator functions in DAX perform row-by-row calculations.\
SUMX, AVERAGEX, COUNTX, MAXX, and MINX evaluate an expression for each
row and then aggregate the result.\
They are used when calculations involve multiple columns and require row
context.
