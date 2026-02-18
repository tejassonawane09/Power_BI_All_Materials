
# Power BI – Basic Concepts

## 1. Power BI Desktop

**What it is**
Power BI Desktop is the main tool used to build reports and dashboards.

**Why it is used**
- Connect to data sources
- Clean and transform data
- Build data models
- Create visuals and dashboards

**Example**
You open Power BI Desktop → connect to Excel sales data → clean data → create charts.

---

## 2. Power Query

**What it is**
Power Query is the data preparation tool inside Power BI.

**Why it is used**
- Fix messy data
- Remove errors
- Transform raw data into usable format

**Example**
Removing blank rows, changing date format, splitting columns.

---

## 3. Data Sources

**What it is**
Data sources are locations from where Power BI gets data.

**Examples**
- Excel / CSV files
- SQL Server / MySQL
- Cloud databases

**Why it is used**
Without data sources, Power BI cannot perform analysis.

---

## 4. Import Mode

**What it is**
Data is copied and stored inside Power BI.

**Why it is used**
- Faster performance
- Works offline
- Best for small/medium data

**Example**
Importing Excel sales data into Power BI.

---

## 5. DirectQuery Mode

**What it is**
Data remains in the database; Power BI queries it live.

**Why it is used**
- Very large datasets
- Real‑time reporting

**Example**
Live connection to SQL Server sales database.

---

## 6. Data Profiling

**What it is**
Understanding the quality of data.

**What you check**
- Missing values
- Errors
- Unique values
- Distribution

**Example**
Finding null revenue values before analysis.

---

## 7. Data Cleaning

**What it is**
Fixing incorrect or unwanted data.

**Examples**
- Removing duplicates
- Replacing nulls
- Fixing wrong values

**Why it is used**
Dirty data leads to wrong business decisions.

---

## 8. Data Transformation

**What it is**
Changing data structure to support analysis.

**Examples**
- Creating new columns
- Splitting product & category
- Creating profit column

---

## 9. Applied Steps

**What it is**
Every transformation done in Power Query is recorded as an Applied Step.

**Why it is used**
- Track changes
- Modify or remove steps

---

## 10. Data Types

**What it is**
Defines the type of data in a column.

**Examples**
- Text
- Whole number
- Decimal number
- Date

**Why it is used**
Correct calculations and visuals depend on data types.

---

## 11. Remove Duplicates

**What it is**
Deletes repeated rows from data.

**Why it is used**
Duplicates increase totals incorrectly.

**Example**
Same invoice entered twice.

---

## 12. Split Column

**What it is**
Breaks one column into multiple columns.

**Example**
`Product - Category` → Product | Category

**Why it is used**
Each column should have one meaning.

---

## 13. Merge Columns

**What it is**
Combines multiple columns into one.

**Example**
First Name + Last Name → Full Name

**Why it is used**
Improves readability.

---

## 14. Group By

**What it is**
Aggregates rows into summary data.

**Examples**
- Monthly sales
- Product‑wise profit

**Why it is used**
To create summary tables before loading.

---

## 15. Append Queries

**What it is**
Stacks multiple tables vertically.

**Example**
January sales + February sales.

**Why it is used**
Same structure, different files.

---

## 16. Merge Queries

**What it is**
Joins tables horizontally.

**Example**
Sales table + Product table using Product ID.

**Why it is used**
To bring related data together.

---

## Interview Tip

If asked:
**“How do you prepare data in Power BI?”**

Answer:
> I use Power Query for data profiling, cleaning, transformation, and structuring before modeling and reporting.

