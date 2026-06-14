Sales Performance Analysis Dashboard 📊
An interactive Power BI dashboard designed to analyze, track, and optimize sales performance. This project transforms raw transactional data into actionable business intelligence, helping stakeholders identify top revenue drivers, monitor key performance indicators (KPIs), and evaluate regional sales health.

🚀 Live Demo & Visuals 
Main Dashboard Page:<img width="1920" height="1080" alt="Screenshot 2026-06-13 234549" src="https://github.com/user-attachments/assets/3d26ec8c-86d1-42f2-9726-8f51ee4201c3" />

Product & Trend Analysis: ![Uploading image.png…]()

🎯 Business Objectives & Key Questions Addressed
The goal of this project is to provide a single source of truth for the sales management team to:

Identify Revenue Trends: Is sales growth accelerating or decelerating over time?
Product Performance: Which specific product categories and items drive the highest profit margins?
Geographical Insights: Where are the highest-performing markets and where are we underperforming?
Customer Segments: Which customer brackets contribute the most to the bottom line?
🛠️ Tech Stack & Tools Used
Power BI Desktop: Dashboard design, report layout, and data visualization.
Power Query (M Language): Data extraction, transformation, profiling, and loading (ETL).
DAX (Data Analysis Expressions): Data modeling, calculated columns, and advanced business measures.
Data Source: [Mention your data source here, e.g., Excel, SQL Server, CSV file, or AdventureWorks dataset].
🔄 Data Architecture & ETL Pipeline
1. Data Cleansing & Transformation (Power Query)
Removed duplicate transaction IDs and dealt with missing values in critical fields.
Standardized data types (e.g., Dates, Currency values).
Created a dedicated, continuous Calendar/Date Table to enable flexible Time Intelligence reporting (YoY, MoM growth).
2. Data Modeling
Built a robust Star Schema to optimize model performance and reporting flexibility:

Fact Table: Fact_Sales (containing transactional rows, revenue, costs, quantities).
Dimension Tables: Dim_Products, Dim_Customers, Dim_Geography, and Dim_Calendar.
Relationships: Defined active 1-to-many (1:*) relationships with unidirectional cross-filtering for optimal DAX performance.
📈 Key Metrics & DAX Measures Created
Here are a few examples of the core analytical metrics calculated for this dashboard:

Total Revenue:
Total Revenue = SUM(Fact_Sales[SalesAmount])
