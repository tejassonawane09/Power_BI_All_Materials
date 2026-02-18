# 📘 DAX Mathematical Functions -- Interview Notes

## 🔹 9️⃣ Mathematical Functions in DAX

### Definition

Mathematical functions in DAX are used to perform numeric calculations
such as rounding, absolute value conversion, exponentiation, and
remainder operations.\
These are mainly used in **Measures** and **Calculated Columns**.

------------------------------------------------------------------------

## 1️⃣ ROUND()

### Definition

Rounds a number to a specified number of decimal places.

### Syntax

ROUND(Number, Num_Digits)

### Example

ROUND(1234.5678, 2)\
Output: 1234.57

### Business Use Case

ROUND(\[Profit %\], 1)

------------------------------------------------------------------------

## 2️⃣ ABS()

### Definition

Returns the absolute (positive) value of a number.

### Syntax

ABS(Number)

### Example

ABS(-5000)\
Output: 5000

### Business Use Case

ABS(\[Actual Sales\] - \[Target Sales\])

------------------------------------------------------------------------

## 3️⃣ POWER()

### Definition

Raises a number to a specified power.

### Syntax

POWER(Number, Power)

### Example

POWER(5, 2)\
Output: 25

### Business Use Case

POWER(1 + \[Growth Rate\], 3)

------------------------------------------------------------------------

## 4️⃣ MOD()

### Definition

Returns the remainder after division.

### Syntax

MOD(Number, Divisor)

### Example

MOD(10, 3)\
Output: 1

### Business Use Case

IF(MOD(Sales\[OrderID\], 2) = 0, "Even", "Odd")

------------------------------------------------------------------------

# 🔥 Common Interview Questions

### Q1: Why do we use ROUND in Power BI?

To control decimal places and improve financial reporting clarity.

### Q2: What is the use of ABS in business reports?

Used in variance analysis to show the magnitude of difference.

### Q3: What does MOD function return?

It returns the remainder after division.

### Q4: Difference between ROUND and formatting in visual?

ROUND changes the actual value, formatting only changes display.

### Q5: Where are mathematical functions mostly used?

In KPI calculations, financial metrics, and business performance
analysis.

------------------------------------------------------------------------

# 🎯 Final Interview Summary

Mathematical functions in DAX help perform numeric operations.\
ROUND controls precision, ABS converts negative values to positive,
POWER performs exponentiation, and MOD returns remainder values.\
These functions are widely used in financial dashboards and KPI
calculations.
