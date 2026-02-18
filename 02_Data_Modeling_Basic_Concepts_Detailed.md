
# Data Modeling – Basic Concepts 

## 1. Fact Table

### What it is
A Fact Table contains **transactional or measurable data**.

### What it usually contains
- Numeric values (Revenue, Cost, Quantity, Profit)
- Foreign keys (Date, Product ID, Region ID)
- Large number of rows
- Repeated values

### Example
**Fact_Sales Table**
- Date
- Product ID
- Region ID
- Revenue
- Cost
- Quantity

### Why it is important
All KPIs and calculations are created from the fact table.

---

## 2. Dimension Table

### What it is
A Dimension Table contains **descriptive attributes** used for filtering and grouping.

### What it usually contains
- Text or categorical values
- Unique rows
- Fewer records than fact table

### Examples
- Product Dimension: Product Name, Category
- Date Dimension: Date, Year, Month
- Region Dimension: Region Name

### Why it is important
Dimension tables allow analysis like:
- Sales by Product
- Profit by Region
- Revenue by Year

---

## 3. Star Schema

### What it is
A Star Schema is a **data model design** where:
- One Fact Table is in the center
- Multiple Dimension Tables are connected to it

### Example Structure
Fact_Sales connected to:
- Dim_Date
- Dim_Product
- Dim_Region

### Why it is used
- Simple and clean structure
- Better performance
- Easier DAX calculations
- Industry standard design

---

## 4. Relationships

### What it is
Relationships define **how tables are linked together**.

### Why it is needed
Without relationships:
- Filters do not work
- Aggregations become incorrect
- Dashboards give wrong results

### Example
- Dim_Product[Product ID] → Fact_Sales[Product ID]
- Dim_Date[Date] → Fact_Sales[Date]

---

## 5. Cardinality (One-to-Many)

### What it is
Cardinality defines **how rows match between tables**.

### One-to-Many Explanation
- One row in dimension table
- Multiple rows in fact table

### Example
- One product appears once in Dim_Product
- Same product appears many times in Fact_Sales

### Why it matters
Correct cardinality ensures accurate filtering and totals.

---

## 6. Cross Filter Direction

### What it is
Cross filter direction controls **how filters flow between tables**.

### Single Direction (Best Practice)
- Filters flow from Dimension → Fact

### Why single direction is recommended
- Avoids ambiguity
- Improves performance
- Prevents incorrect calculations

---

## 7. Active and Inactive Relationships

### Active Relationship
- Used by default in calculations
- Shown as a solid line

### Inactive Relationship
- Not used unless explicitly activated
- Shown as a dotted line

### Example
Order Date (Active) and Ship Date (Inactive) both exist in sales data.

---

## 8. Model View

### What it is
Model View displays **tables and relationships visually**.

### Why it is used
- Create and manage relationships
- Check schema design
- Validate cardinality and filter direction

### Importance
A clean model view indicates a professional Power BI report.

---

## 9. Hide Columns

### What it is
Hiding columns removes them from report view without deleting data.

### Why it is used
- Avoid confusion
- Keep fields pane clean
- Prevent incorrect field usage

### Example
Hide Product ID in Fact table when Product Name is available in Dimension table.

---

## Interview Tip

**Question:** How do you design data models in Power BI?

**Answer:**
I use a star schema with a central fact table and supporting dimension tables, create one-to-many relationships with single-direction filters, and hide unnecessary columns for a clean model.

---

