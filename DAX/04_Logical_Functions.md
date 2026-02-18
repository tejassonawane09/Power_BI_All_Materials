
# 📘 DAX Logical Functions – Power BI 

## 🔹 Definition
Logical functions in DAX are used to apply conditions and return results based on TRUE or FALSE logic.  
They are commonly used in Measures and Calculated Columns to implement business rules.

---

# 1️⃣ IF()

## ✅ Definition
Checks a condition and returns one value if TRUE and another if FALSE.

## ✅ Syntax
IF(Logical_Test, Value_if_True, Value_if_False)

## ✅ Example
Salary Band =
IF(Employees[Salary] > 50000, "High", "Low")

---

# 2️⃣ SWITCH()

## ✅ Definition
Evaluates an expression against multiple values and returns matching result.

## ✅ Syntax
SWITCH(Expression,
       Value1, Result1,
       Value2, Result2,
       Else_Result)

## ✅ Example
Grade =
SWITCH(
    TRUE(),
    Students[Marks] >= 80, "A",
    Students[Marks] >= 60, "B",
    Students[Marks] >= 40, "C",
    "Fail"
)

---

# 3️⃣ AND()

## ✅ Definition
Returns TRUE if both conditions are TRUE.

## ✅ Syntax
AND(Condition1, Condition2)
OR
Condition1 && Condition2

## ✅ Example
Bonus Eligible =
IF(Employees[Salary] > 50000 && Employees[Experience] > 5, "Yes", "No")

---

# 4️⃣ OR()

## ✅ Definition
Returns TRUE if at least one condition is TRUE.

## ✅ Syntax
OR(Condition1, Condition2)
OR
Condition1 || Condition2

## ✅ Example
Discount Eligible =
IF(Sales[Amount] > 10000 || Sales[CustomerType] = "Premium", "Yes", "No")

---

# 5️⃣ NOT()

## ✅ Definition
Reverses the logical result.

## ✅ Syntax
NOT(Condition)

## ✅ Example
Inactive Customer =
IF(NOT(Sales[Status] = "Active"), "Inactive", "Active")

---

# 🔥 Common Interview Questions

## Q1: Difference between IF and SWITCH?
IF is used for simple TRUE/FALSE conditions.
SWITCH is used when multiple conditions need to be checked.

## Q2: Why use SWITCH(TRUE())?
It allows checking multiple logical conditions in sequence.

## Q3: What is the shortcut for AND and OR?
AND → &&
OR → ||

## Q4: Can logical functions be used in Measures?
Yes, logical functions work in both Measures and Calculated Columns.

## Q5: Real Business Use Case?
Logical functions are used for KPI classification, eligibility rules, grading systems, and profit/loss status.

---

# 🔹 Final Interview Summary
Logical functions in DAX help apply business logic inside reports.  
IF handles basic conditions, SWITCH handles multiple conditions, AND/OR combine conditions, and NOT reverses logic.
