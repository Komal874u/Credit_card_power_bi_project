Credit Card Financial & Customer Analysis Dashboard
📌 Project Overview
This project involves the development of a comprehensive Power BI dashboard that provides real-time, actionable insights into credit card transactions and customer demographics. The dashboard enables stakeholders to effectively monitor financial performance, track operational metrics, and understand consumer behavior to drive strategic, data-backed decisions.

🛠️ Tech Stack & Skills
Business Intelligence: Power BI Desktop

Data Modeling: Star Schema, Relationship Mapping

DAX (Data Analysis Expressions): Custom measures for KPIs, YTD tracking, and dynamic segmentations.

Data Transformation: Power Query (ETL process, data cleaning, type casting, custom column additions)

📊 Dashboard Architecture & Key Insights
The solution is divided into two analytical views to separate core business performance from consumer profiling:

1. Credit Card Transaction Report (Financial View)
This view focuses on the macroeconomic health, revenue streams, and volume metrics of the credit card portfolio.

Core KPIs: * Total Revenue: $12M

Total Interest Earned: $7.84M

Total Transaction Amount: $45M

Total Transaction Count: 12K

Quarterly Performance (Revenue By QTR): Monitors seasonal fluctuations. Revenue peaks in Q1 and Q3 ($4.3T scale represented in raw unformatted data) with stable transaction volume trends.

Card Category Dominance: Blue Category cards are the primary revenue driver ($11.2T), significantly outperforming Silver, Gold, and Platinum tiers.

Revenue by Expenditure & Usage: * Bills ($3.4T) and Food ($2.9T) represent the highest swipe categories.

Swipe is the preferred method of transaction ($9.0T) compared to Chip ($6.0T) and Online ($1.0T).

Demographic Streams: Businessmen shape the majority of the job profile revenue ($8T), while Graduates represent the largest share by education level (38.87%).

2. Credit Card Customer Report (Demographic View)
This view dives deep into consumer segments, behavior patterns, and customer-centric health metrics.

Core KPIs:

Revenue: $12M

Total Interest: $7.84M

Total Customer Income: $576M

Customer Satisfaction Score (CSS): 3.19 / 5.0

Weekly Trends (Revenue By Week): A dual-line time-series visualization tracking revenue trends across 2023, identifying cyclical spending spikes.

Age & Gender Insights: * The 30-40 age cohort is the highest spend group ($7T Female / $9T Male).

Overall revenue contribution leans slightly higher towards Male clients ($88.7M vs. $71.9M raw metric matrix).

Income & Marital Demographics: * High-income individuals drive the bulk of portfolio revenue ($5T Female / $8T Male).

Married individuals generate the highest revenue compared to Single or Unknown statuses.

Geographic Distribution: Top 5 performing states are highlighted, with NY (New York) and TX (Texas) leading the transaction volumes.

📈 Key DAX Measures & Data Transformations
(You can customize this section with your actual code. Below are examples of what you likely implemented)

Age & Income Binning: Implemented conditional DAX/Power Query grouping to cluster customers cleanly into 20-30, 30-40, 60+ and Low, Medium, High economic bands.

Revenue Generation: ```dax
Revenue = SUM('Credit Card Data'[Annual_Fees]) + SUM('Credit Card Data'[Total_Trans_Amt]) + SUM('Credit Card Data'[Interest_Earned])
