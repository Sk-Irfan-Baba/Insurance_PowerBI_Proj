# 🛡️ Unlimited Insurance Co. - Business Intelligence Dashboard

![Power BI Dashboard](image_ba0907.jpg)
*(Note: Replace 'image_ba0907.jpg' with the actual path to your screenshot in the repo)*

## 📌 Project Overview
This project involves a comprehensive data analysis for "Unlimited Insurance Company." The goal was to transform raw historical data into an interactive dashboard that allows stakeholders to monitor key performance indicators (KPIs) such as Premium generation, Claim settlements, and Coverage distribution across different policy types and demographics.

The dashboard provides a high-level view of the company's financial health and customer demographics, enabling data-driven decisions regarding policy pricing and risk management.

## 🔄 Data Architecture & Workflow
Unlike a standard Power BI project, this solution mimics a real-world enterprise environment by utilizing a SQL database as the intermediary warehouse.

**The Pipeline:**
1.  **Source Data:** Raw data received in CSV format (Customers, Claims, Policies).
2.  **ETL & Storage (SQL Server):**
    * Imported CSV files into **MS SQL Server**.
    * Performed initial data quality checks and type casting within SQL.
    * Served as the "Source of Truth" for the BI tool.
3.  **Visualization (Power BI):**
    * Connected Power BI directly to the SQL Server database (Import Mode).
    * Modeled data using a Star Schema.
    * Built DAX measures and interactive visuals.

## 📊 Key Insights & Features
* **Financial Health:** Tracking Total Premium (**2.99M**) vs. Total Claim Amount (**8.41M**) and Coverage.
* **Policy Analysis:** Breakdown of premiums by `Policy Type` (Travel, Health, Auto, etc.) identifying "Travel" as the leading revenue generator.
* **Demographics:** Analysis of customer distribution by Gender and Age Group (Adult, Elder, Young Adult).
* **Claims Status:** A clear view of the claims pipeline (Rejected vs. Settled vs. Pending) to monitor operational efficiency.
* **Customer Churn:** Visualizing Active vs. Inactive policies (Currently ~21% Inactive).

## 🛠️ Tech Stack
* **Database:** Microsoft SQL Server
* **ETL:** SQL (Bulk Insert/Import Wizard)
* **Visualization:** Microsoft Power BI
* **Data Modeling:** Star Schema, DAX

## 🧠 Approach & Methodology
1.  **Data Staging:** Loaded raw CSVs into SQL Server tables (`tbl_Customers`, `tbl_Claims`, `tbl_Policies`).
2.  **Data Modeling:** Established relationships between tables in Power BI (One-to-Many relationships using `CustomerID` and `PolicyID`).
3.  **DAX Calculations:** Created measures for:
    * Total Premium Amount
    * Total Coverage
    * Count of Claims by Status
4.  **Dashboard Design:** Designed a layout focused on accessibility, using a consistent color theme and clear KPI cards for top-level metrics.

## 🚀 Future Improvements
* **Drill-through Filters:** Implementing drill-through functionality to inspect specific Claim IDs without cluttering the main dashboard.
* **Trend Analysis:** Adding a Date Table to visualize premiums and claims over time (MoM, YoY) to identify seasonality.
* **Visual Logic:** Converting the "Age Group" line chart to a Clustered Bar chart for better categorical representation.

## 📂 File Structure
* `Data/`: Contains the sample CSV files (if public) or SQL scripts to generate the schema.
* `SQL_Scripts/`: Queries used for data validation or transformation.
* `Insurance_Dashboard.pbix`: The Power BI file.

---
**Author:** [Your Name]  
**LinkedIn:** [Link to your Profile]
