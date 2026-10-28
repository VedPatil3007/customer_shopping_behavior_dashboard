👨🏻‍💻 Customer Shopping Behavior Analysis | End-to-End Data Analytics Project
This project represents a complete, industry-standard, end-to-end data analytics workflow designed to mirror the real-world responsibilities of professional data analysts in e-commerce and retail environments. The project covers every stage of the data pipeline: from initial Python data cleaning and PostgreSQL database integration to complex SQL business analysis and interactive Power BI dashboarding.

🎯 Business Problem Statement
A leading retail company wants to better understand its customers' shopping behavior to improve sales, customer satisfaction, and long-term loyalty. Management has noticed changing purchasing patterns across demographics, product categories, and sales channels. They require data-driven clarity on how factors such as discounts, review ratings, seasonal trends, and payment preferences influence consumer decisions and drive repeat purchases.   

❓ Overarching Business Question:
"How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?"

📌 Project Deliverables
Data Preparation & Modeling (Python): Clean, transform, and impute raw dataset attributes for database loading.
Business Data Analytics (PostgreSQL): Model data into structured tables, simulate real transactions, and run analytical queries to extract insights on loyalty and spend drivers.
Interactive Dashboarding (Power BI): Build a dynamic executive dashboard showcasing key KPIs, demographic filters, and visual trends.
Strategic Reporting & Recommendations: Synthesize analytical findings into actionable business recommendations for stakeholders.
GitHub Documentation: Maintain a fully structured portfolio repository containing code scripts, SQL queries, DAX formulas, and visual reports.

🏗️ Technical Architecture & Workflow
<pre><code>
┌─────────────────┐      ┌──────────────────────────┐      ┌─────────────────────────┐      ┌──────────────────────┐
│  Raw Data Source│ ───► │   Data Cleaning & Prep   │ ───► │    Database Storage     │ ───► │ Business BI & Visuals│
│  (3,900 rows)   │      │      ( Pandas)           │      │      (PostgreSQL)       │      │     (Power BI )      |
└─────────────────┘      └──────────────────────────┘      └─────────────────────────┘      └──────────────────────┘
</code></pre>

📊 Dataset Summary
Total Records: 3,900 transaction records
Attributes: 18 demographic & behavioral features
Key Features:
Demographics: Age, Gender, Location, Subscription Status
Purchase Details: Item Purchased, Category, Purchase Amount ($), Season, Size, Color
Behavioral Metrics: Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

🛠️ Tech Stack & Tools Used
Language: Python (Pandas, NumPy, SQLAlchemy)
Database: PostgreSQL (SQL Querying, Aggregations, Window Functions, CTEs)
Data Visualization: Power BI Desktop (DAX, Interactive Slicers, KPI Cards, Cross-Filtering)
Documentation & Version Control: Git, GitHub, Markdown

🔍 Key Project Stages & Highlights
1. Data Cleaning & Feature Engineering (Python)
Missing Value Imputation: Handled 37 missing values in the Review Rating column by imputing the median rating of each specific product category to preserve statistical distribution.
Standardization: Converted all dataset column headers into clean snake_case naming conventions.
Feature Engineering:
Binned customer ages into categorical age_group tiers (Young Adult, Middle-aged, Adult, Senior).
Derived purchase_frequency_days to measure customer re-engagement windows.
Redundancy Clean-up: Evaluated overlap between Discount Applied and Promo Code Used to streamline tracking attributes.
Automated Pipeline: Connected Python directly to PostgreSQL using SQLAlchemy to automatically populate database tables.
2. Deep-Dive Business Analytics (PostgreSQL)
A total of 10 strategic business queries were executed. Highlights include:
Customer Segmentation (CTE Analysis): Categorized buyers into New (1 purchase), Returning (2–10 purchases), and Loyal (>10 purchases) segments:
Loyal: 3,116 customers
Returning: 701 customers
New: 83 customers
Gender Revenue Breakdown:
Male: $157,890 total revenue
Female: $75,191 total revenue
Discount Dependency: Identified top product categories driven by discounts (e.g., Hats at 50.00% discount dependency, Sneakers at 49.66%).
Subscription & Spend Analysis:
Non-subscribers generated $170,436 in revenue vs. $62,645 from subscribers. Average spend remained consistent (~$59.49 vs $59.87), indicating subscriptions currently don't drive higher basket size.
Top Products per Category: Leveraged DENSE_RANK() window functions to rank top-selling products across Clothing, Accessories, Footwear, and Outerwear.
3. Dashboard & Visual Insights (Power BI)
Built a dynamic 2-page executive dashboard displaying:
Key Performance Indicators (KPIs): Total Customers (3.9K), Average Purchase Amount ($59.76), Average Review Rating (3.75).
Demographic Breakdown: Interactive slicers for Subscription Status, Gender, Category, and Shipping Types.
Behavior Analysis: Visualized category distribution, sales by age group, and subscription ratios.

💡 Strategic Business Recommendations   
Overhaul Subscription Incentives: Current subscribers spend the same average amount per transaction as non-subscribers. Introduce exclusive perks (e.g., free shipping, loyalty point multipliers) to increase average order value (AOV) for subscribers.  

Targeted Loyalty Programs: Over 80% of buyers fall into the Loyal segment (>10 purchases). Implement tier-based rewards to prevent churn among high-value repeat customers.  

Discount Strategy Optimization: Products like Hats, Sneakers, and Coats rely heavily on discounts (>48% discount rate). Restructure promotions to avoid margin erosion while preserving sales volume.

Demographic Expansion: Young Adults and Middle-aged segments contribute the highest total revenue ($62.1K and $59.1K). Focus acquisition campaigns on these core demographics.  
