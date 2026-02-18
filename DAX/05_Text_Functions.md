# 📘 DAX Text Functions -- Interview Notes

## 🔹 Definition

Text functions in DAX are used to manipulate, extract, combine, and
analyze text (string) values inside calculated columns or measures.

------------------------------------------------------------------------

# 1️⃣ CONCATENATE()

## Definition

Joins two text values into one string.

## Syntax

CONCATENATE(Text1, Text2)

Alternative: Text1 & Text2

## Example

Full Name = Employees\[FirstName\] & " " & Employees\[LastName\]

## Interview Points

-   Joins only 2 arguments at a time
-   '&' operator is preferred
-   Used for creating full names, IDs, labels

------------------------------------------------------------------------

# 2️⃣ LEFT()

## Definition

Extracts specified number of characters from the left side of a text.

## Syntax

LEFT(Text, Number_of_Characters)

## Example

Product Prefix = LEFT(Products\[ProductCode\], 3)

## Interview Points

-   Used for code splitting
-   Useful in ID formatting

------------------------------------------------------------------------

# 3️⃣ RIGHT()

## Definition

Extracts specified number of characters from the right side of text.

## Syntax

RIGHT(Text, Number_of_Characters)

## Example

Product Number = RIGHT(Products\[ProductCode\], 3)

## Interview Points

-   Used for extracting numeric suffix
-   Common in data cleaning

------------------------------------------------------------------------

# 4️⃣ MID()

## Definition

Extracts text from middle based on starting position and length.

## Syntax

MID(Text, Start_Position, Number_of_Characters)

## Example

Year Extract = MID(Employees\[EmpCode\], 4, 4)

## Interview Points

-   Position starts from 1
-   Used for parsing structured codes

------------------------------------------------------------------------

# 5️⃣ LEN()

## Definition

Returns total number of characters in a text string.

## Syntax

LEN(Text)

## Example

Name Length = LEN(Employees\[FirstName\])

## Interview Points

-   Counts spaces also
-   Used for validation and data quality checks

------------------------------------------------------------------------

# 🔥 Common Interview Questions

### Q1: Difference between LEFT and MID?

LEFT extracts from beginning.\
MID extracts from any position.

### Q2: Can CONCATENATE join 3 columns?

No. Use '&' operator for multiple joins.

### Q3: Does LEN count spaces?

Yes.

### Q4: Where are text functions mostly used?

Mostly in calculated columns for formatting and data cleaning.

------------------------------------------------------------------------

# 🎯 Final Interview Summary

Text functions in DAX are used to manipulate string values.\
CONCATENATE joins text, LEFT and RIGHT extract characters, MID extracts
from middle, and LEN counts characters.\
They are mainly used for formatting, ID creation, and data cleaning in
business reports.
