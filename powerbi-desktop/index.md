# PowerBI Desktop


An Introduction and reference document for PowerBI Desktop

<!--more-->

# PowerBI

## Introduction PowerBI Desktop

{{< admonition type=abstract title="Abstract" open=false >}}
Installing PowerBI, exploring the PowerBI workflow, comparingn PowerBI vs. Excel.
{{< /admonition >}}

### Meet Power BI

**Image:** *Magic Quadrant for Analytics and Business Intelligence Plattforms*

Power BI is a standalone Microsoft business intelligence product, which includes both desktop and web-based applications for loading, modeling, and visualizing data

More information at {{< link "powerbi.microsoft.com">}}

### Why Power BI

- Connect, transform and analyze *millions* of rows of data
  - Access data from virtually anywhere (database tables, flat files, cloud services, folders, etc), and create fully automated data shaping and loading (ETL) procedures
- Build relational models to blent data from multiple sources
  - Create table relationship to analyze holistic performance across an entire data model
- Define complex calculations using Data Analysis Expressions (DAX)
  - Enhance datasets and enable advanced analytics with powerful and portable DAX expressions
- Visualize data with interactive reports and dashboards
  - Build custom business intelligence tools with best-in-class visualization and dashboard features
- Power BI is the industry leader among BI platforms
  - Microsoft Power BI is intuitive, powerful and FREE to get started

### Power BI vs Power Excel

Power Excel and Power BI are built on top of the **exact same engine!**
- Power BI takes the same data shaping, modeling and analytics capabilities and adds **new reporting and publishing tools**
- Transitioning is easy; one can import an **entire data model** directly from Excel!

|Power Excel|                 |Power BI                 |
|:----------|-----------------|:------------------------|
|PivotTables|Data Shaping     |Report View              |
|PivotCharts|Data Modeling    |Custom Visualization Tools|
|Power Map/ PowerView|Calculated Fields|Publishing & Collaboration Options|

### The Power BI Interface

**Three Core Views:**

- Report
- Data
- Relationship

### The Power BI Workflow

1. Connect, shape and tranform raw **data**
2. Build table **relationships** to tie sources together
3. Design interactive **reports** to explore and visualize data

### Helpful Resources

The Microsoft Power BI blog publishes monthly summaries to showcase new features
[Microsoft Power BI blog](https://powerbi.microsoft.com/en-us/blog/)

The Mircosoft Power BI YouTube Channel publishes demos, feature summaries, and advanced tutorials
[Microsoft Power BI YouTube Channel](https://www.youtube.com/user/mspowerbi)

[Guy in a Cube](https://www.youtube.com/c/GuyinaCube/videos)

Power BI User Group are communities of users, which include both local meet-ups and helpful online forms
[Power BI User Groups](https://www.pbiusergroup.com/home)

## Connecting and Shaping Data

{{< admonition type=abstract title="Abstract" open=false >}}
Connecting to source data, shaping and transforming tables, editing, merging and appending queries.
{{< /admonition >}}

### Types of Data Conecctors

Power BI can connect to virtually **any** type of source data, includeing:

- **Flat files & Folders** (csv, text, xls, ...)
- **Databases** (SQL, Access, Oracle, IBM, Azure, ...)
- **Online Services** (Sharepoint, GitHub, Dynamics 365, Google Analytics, Salesforce, Power BI Service, ...)
- **Others** (Web feeds, R scripts, Spark, Hadoop, ...)

### Query Editor

Top to bottom 

**Query Editing Tools** (Table transformations, calculated columns, ...)

**Formular Bar** (M code)

**Query List**

**Table Name & Properties**

**Table Name & Properties**

**Applied Steps** (like a macro)

### Query Editing Tools

The *HOME* tab includes **general settings** and **common table transformation tools**

The *TRANSFORM* tab includes tools to **modify existing columns** (splitting/grouping, transposing, extracting text, ...)

The *ADD COLUMN* tools **create new columns** (based on conditional rules, text operations, calculations, dates, ...)

### Basic Table Tranformations

1. **Choose or remove columns**
{{< admonition type=tip title="Tip" open=false >}}
Use the *Remove Other Columns* option if one always want a specific set
{{< /admonition >}}
2. **Keep or removes rows**
{{< admonition type=tip title="Tip" open=false >}}
Use the *Remove Duplicates* option to create a new loopup table from scratch
{{< /admonition >}}
3. **Sort values** (A-Z, Low-High, ...)
4. **Change data type** (date, $, %, text, ...)
5. **Promote header row**
6. **Duplicate, move & rename** columns
{{< admonition type=tip title="Tip" open=false >}}
Right-click the column header to access common tools
{{< /admonition >}}

### Text-Specific Tools

1. **Split a text column** based on either a specific delemiter or a number of characters 
2. **Format a text column** to upper, lower or proper case, or add a prefix or suffix
{{< admonition type=tip title="Tip" open=false >}}
Use *Trim* to eliminate leading & trailing spaces, or *Clean* to remove non-printable characters
{{< /admonition >}}
1. **Extract characters from a text** based on fixed lengths, first/last, ranges or delimiters
{{< admonition type=tip title="Tip" open=false >}}
Select two or more columns to **merge** (or **concatenate**) fields
{{< /admonition >}}


{{< admonition type=warning title="Warning" open=false >}}
One can access many of these tools in both the **Transform** and **Add Column** menus. 
The difference is whether one want to **add a new column** or **modify an existing one**
{{< /admonition >}}

### Number-Specific Tools

1. **Statistics functions** allow one to evaluate basic stats for the selected column basic stats for the selected column (sum, min/max, average, count, countdistinct, ..)
{{< admonition type=note title="Note" open=false >}}
These tools return a *SINGLE* vlaue, and are commonly used to explore a table rather than prepare it for loading
{{< /admonition >}}
1. **Standard, Scientific** and **Trigonometry** tools allow one to apply standard operations (addition, multiplicatino, division, ...) or more advanced calculations (power, logarith, sine, tangent, ...) to each value in a column
{{< admonition type=note title="Note" open=false >}}
Unlike the statistics options, these tools are applied to each individual row in the table
{{< /admonition >}}
2. **Information** tools allow one to define binary flags (TRUE/FALSE or 1/0) to mark each row in a column as even, odd positive or negative

### Data-Specific Tools

1. **Date & Time** tools are relatively straight-forward, and include the following options:
   - **Age:** Difference between the current time and the date in each row
   - **Date Only:** Removes the time component of a data/time field
   - **Year/Month/Quarter/Week/Day:** Extracts individual components from a date field (Time-specific options include Hour, Minute, Second, ...)
   - **Earliest/Latest:** Evaluates the earliest or latest date from a column as single value (can only be accessed from the *Transform* menu)
{{< admonition type=note title="Note" open=false >}}
One will almost always want to perform these operations from the *Add Column* menu to build out new fields, rather than transforming an individual date/time column
{{< /admonition >}}

{{< admonition success "Pro" false>}}
Load up a table containing a **single date column** and use Date tools to buld out an **entire calendar table**
{{< /admonition >}}

### Creating a Basic Calendar Table

Use pre-defined **Date** options in the *Add Column* menu to quickly build out a calendar table out a calendar table from a list of dates

### PRO TIP Creating a Rolling Calendar

1. Create a new, blank query (**Get Data** > **Blank Query** or **New Source** > **Blank Query**)
2. In the formula bar, generate a starting date by entering a **literal** (in YYYY, MM, DD format)
3. Click the **fX** icon to add a new custom step, and enter the following formula exactly as shown
4. Convert the resulting list into a Table (**List Tools** > **To Table**) and format the column as a **Date**
5. Add calculated Date columns (Year, Month, Week, ...) as necessary using the **Add Column** tools

### Adding Index Columns

1. **Index Columns** contain a list of sequential values that can be used to identify each unique row in a table (typically starting from 0 or 1)

    These columns are often used to create **unique IDs** that can be used to form relationships between tables

### Adding Conditional Columns

1. **Conditional Columns** allow one to define new fields based on logical rules and conditions (IF/THEN statements)

    In a case one can create a new conditional column called *QuantityType*, which depends on the values in the *OrderQuantity* column, as follows:
    - If OrderQuantity = 1, QuantityType = **Single Item**
    - If OrderQuantity >1, QuantityType = **Multiple Items**
    - Otherwise QuantityType = **Other**

### Grouping & Aggregating Data

1. **Group By** allows one to aggregate the data at a different level (i.e. transform daily data into monthly, roll up transaction-level data by sotre, ...)

In a case one can transform a daily, transaction-level table into a summary of *TotalQuantity* rolled up by *ProductKey*

{{<admonition note "Note" false>}}
Any field not specified in the Group By settings are lost
{{</admonition>}}

### Grouping & Aggregating Data Advanced

This time one transform the daily transaction-level table into a summary of *TotalQuantity* aggregated by both *ProductKey* and *CustomerKey* (using the advanced option in the dialog box)

{{<admonition note "Note" false>}}
This is similar to creating a PivotTable in Excel and pulling in *Sum of OrderQuantity* with *ProductKey* and *CustomerKey* as row labels
{{</admonition>}}

### Pivoting & Unpivoting

### Merging Queries

### Appending Queries

### Data Source Settings

### Modifying Queries

### Refreshing Queries

### Defining Data Categories

### Defining Hierarchies

### PRO TIP: Importing Models From Excel

### Best Practice: Connecting & Shaping Data

## Creating a Data Model

{{< admonition type=abstract title="Abstract" open=false >}}
Building relational models, creating table relationships, understanding cardinality, exploring filter flow.
{{< /admonition >}}

## Adding Calculated Fields with DAX

{{< admonition type=abstract title="Abstract" open=false >}}
Understanding DAX syntax, adding calculated columns and measures, writing common formulas and functions.
{{< /admonition >}}

## Visualizing Data with Reports

{{< admonition type=abstract title="Abstract" open=false >}}
Inserting charts and visuals, customizing formats, editing interactions, applying filters and bookmarks.
{{< /admonition >}}
