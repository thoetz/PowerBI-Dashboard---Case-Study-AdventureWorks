# PowerBI-Dashboard---Case-Study-AdventureWorks
Files thought process and PowerBI Dashboard for the Case Study of AdventureWorks as part of a udemy course. Visit the AdventureWorks Report.pbix file to view the dashboard and PowerBI file.

# Introduction
This README.md document outlines the process and steps taken in a Power BI course, focusing on data modelling, data preparation, analysis, and visualization. The case study follows AdventureWorks, a fictional bike retailer operating internationally. Our ultimate task is to help them build a dashboard for monitoring sales, customers and plenty more data to help them uncover insights about their business. It covers various aspects, including data normalization, DAX (Data Analysis Expressions) calculations, and the creation of insightful visualizations in PowerBI.

# Table of Contents
1. [Introduction](#introduction)
2. [Section 1: Connecting Data](#section-1-connecting-data)
   - [My Process before Importing Data to Power Query](#my-process-before-importing-data-to-power-query)
   - [Objective 1: Table Transformations](#objective-1-table-transformations)
   - [Objective 2: Further Data Cleaning and Preparation](#objective-2-further-data-cleaning-and-preparation)
   - [Objective 3: Grouped and Aggregated Sales Data](#objective-3-grouped-and-aggregated-sales-data)
3. [Section 2: Data Modeling](#section-2-data-modeling)
   - [Normalize the Data](#normalize-the-data)
   - [Objective 4: Connecting Tables](#objective-4-connecting-tables)
   - [Objective 5: Diagnose and Hide Foreign Keys](#objective-5-diagnose-and-hide-foreign-keys)
   - [Objective 6: Customize Data Format](#objective-6-customize-data-format)
   - [Objective 7: Creating Hierarchies](#objective-7-creating-hierarchies)
4. [Section 3: Creating Calculated Fields with DAX](#section-3-creating-calculated-fields-with-dax)
   - [Objective 8: Create New Measures](#objective-8-create-new-measures)
   - [Objective 9: Total Customers and Return Rate](#objective-9-total-customers-and-return-rate)
   - [Objective 10: Utilize Logical Functions](#objective-10-utilize-logical-functions)
   - [Objective 11: Utilize Text Functions](#objective-11-utilize-text-functions)
   - [Objective 12: Utilize Date/Time Functions](#objective-12-utilize-date-time-functions)
   - [Objective 13: Calculate Weekend Orders](#objective-13-calculate-weekend-orders)
   - [Objective 14: Analyze Bike Returns](#objective-14-analyze-bike-returns)
   - [Objective 15: Use ALL() Function](#objective-15-use-all-function)
   - [Objective 16: Calculate High Ticket Orders](#objective-16-calculate-high-ticket-orders)
   - [Objective 17: Clean Up Data](#objective-17-clean-up-data)
   - [Objective 18: Analyze Profit](#objective-18-analyze-profit)
   - [Objective 19: Time Intelligence Formulas](#objective-19-time-intelligence-formulas)
   - [Objective 20: Track Month Over Month and Year Over Year](#objective-20-track-month-over-month-and-year-over-year)
5. [Section 4: Data Visualization](#section-4-data-visualization)
   - [Objective 21: Revisit Dashboard Goals](#objective-21-revisit-dashboard-goals)
   - [Objective 22: Dashboard Tasks](#objective-22-dashboard-tasks)
6. [Section 5: PowerBI AI](#section-5-powerbi-ai)
   - [Objective 23: Establish and Complete Dashboard Tasks](#objective-23-establish-and-complete-dashboard-tasks)
   - [Objective 24: Analyze Return Rate](#objective-24-analyze-return-rate)


## Section 1: Connecting Data
### My Process Before Importing Data to Power Query
1. **Get Organized**
   - Define clear and intuitive table/query names from the start.
   - Establish an organized file folder structure to avoid changes to filenames or paths.
2. **Disable Report Refresh for Statistic Data Sources**
   - No need to constantly refresh data sources that don’t change.
3. **Load Only What's Needed**
   - For larger tables or models, load only what's necessary (e.g., don't load hourly if using daily data).
4. **Confirm Data Types**
   - Confirm that data types are correct.

### Objective 1: Table Transformations
- Create 2 new queries to connect the Product Category Lookup and Product Sub Category Lookup fields.
- Add a new column to extract all characters before the dash of SKU and ProductName.

### Objective 2: Further Data Cleaning and Preparation
- Load customer lookup table.
- Clean data to eliminate errors in customer key.
- Replace 0’s in the Gender Column with NA.

### Objective 3: Grouped and Aggregated Sales Data
- Advanced group-by query to see total sales per product and customer.

## Section 2: Data Modeling
- **Normalize the Data:**
  - Reduce redundancy/duplicates, and decrease table sizes.
  - Reduce errors and anomalies.
  - Simplify queries.

### Objective 4: Connecting Tables
- Connect facts table (Sales Data) with territory lookup, customer lookup, calendar lookup, and product lookup tables using a Star Schema.
- Connect 3 product tables using a Snowflake Schema.

### Objective 5: Diagnose and Hide Foreign Keys
- Investigate and fix issues with the model.
- Hide foreign keys to prevent mistakes.

### Objective 6: Customize Data Format
- Change dates to display in a short format.
- Adjust currency columns to 2 decimals.
- Format Country and Continent fields.

### Objective 7: Creating Hierarchies
- Create hierarchies for territory fields.
- Create a hierarchy based on the start of the year field.

## Section 3: Creating Calculated Fields with DAX 
### Objective 8: Create New Measures
- Quantity Sold (SUM())
- Quantity Returned (SUM())
- Average Retail Price (AVERAGE())
- Total Returns (COUNT())

### Objective 9: Total Customers and Return Rate
- Create a measure for total customers.
- Create a measure for return rate.

### Objective 10: Utilize Logical Functions
- Use IF statements and Switch functions to categorize customers based on income and education level.

### Objective 11: Utilize Text Functions
- Create new columns using text functions to abbreviate months, concatenate customer names, and extract SKU categories.

### Objective 12: Utilize Date/Time Functions
- Create columns for day of the week, weekend classification, and birth year.

### Objective 13: Calculate Weekend Orders
- Create a measure to calculate orders on weekends.

### Objective 14: Analyze Bike Returns
- Create measures and a matrix to analyze returns and sales for bikes.

### Objective 15: Use ALL() Function
- Create measures and a matrix to show the percentage of returns by product category.

### Objective 16: Calculate High Ticket Orders
- Create a measure for high ticket orders.

### Objective 17: Clean Up Data
- Remove retail price and revenue columns from sales data.
- Combine them into new measures using SUMX and RELATED.

### Objective 18: Analyze Profit
- Create measures for total cost and total profit.

### Objective 19: Time Intelligence Formulas
- Create YTD and previous month's revenue

 measures.
- Create a 10-day rolling revenue measure.

### Objective 20: Track Month Over Month and Year Over Year
- Create measures for the previous month's returns, profit, and orders.
- Create order and profit target measures.
- Create a 90-day rolling profit measure.

## Section 4: Data Visualization
- **To see the completed dashboard and included data visualizations, visit the AdventureWorks Report.pbix document.**

### Objective 21: Revisit Dashboard Goals
- Track KPIs.
- Compare regional performance.
- Analyze product-level trends.
- Identify high-value customers.

### Objective 22: Dashboard Tasks
- Product Detail Report:
  - Conditionally formatted gauges on the product detail screen.
  - Create measures to measure the gap to target value for three metrics.
  - Create an area chart for weekly profit and returns.

- Interaction and Navigation:
  - Add a slicer to drill into the continent.
  - Edit report interactions on the exec page.
  - Update customer report page interactions.

- Additional Features:
  - Add navigation menu to each page.
  - Add slicer pop-out menu to exec sum page.
  - Add numeric range parameter to Product detail page for price adjustment percentage.
  - Add fields parameter to Product detail page.
  - Update line chart colors and parameters on the customer report page.
  - Create custom tooltips for orders by category chart on the exec page.

## Section 5: PowerBI AI
### Objective 23: Establish and Complete Dashboard Tasks
- **Anomaly Detection:**
  - Smart Narratives: Create customizable AI-generated text summaries based on reports or visuals.
  - Q&A visuals: Allow users to explore and visualize data using intuitive natural language prompts.
  - Decomposition Trees: Visualize how data is distributed across multiple dimensions.
  - Key Influencers: Understand the factors that drive specific metrics or outcomes.

### Objective 24: Analyze Return Rate
- Use a decomposition tree to identify the root cause of the higher-than-expected return rate.
