# cartiq-retail-analytics

"How can a retail company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?"


## 📌 Project Overview
CartIQ is an end-to-end data analytics project that dives deep into the shopping behavior of 3,900+ retail customers to surface actionable business intelligence. By combining Python-based data engineering, SQL-driven analysis, and an interactive Power BI dashboard, this project transforms raw transactional data into strategic decisions around revenue, loyalty, discounts, and product performance.

## 🎯 Business Problem
A leading retail company observed shifting purchasing patterns across demographics, product categories, and sales channels. Management needed clarity on:

Which customer segments drive the most revenue?
Do discounts help or hurt margins?
What separates a one-time buyer from a loyal subscriber?
Which products deserve more marketing investment?
How does shipping preference affect spending behavior?


## 📂 Project Structure
CartIQ/
│
├── 📓 Customer_behavior.ipynb       # Data cleaning & feature engineering
├── 🗄️ Customer_Behavior.sql         # 10 business-driven SQL queries
├── 📊 Dashboard.png                 # Power BI dashboard snapshot
└── 📄 README.md

## 🛠️ Tech Stack
ToolPurposePython (Pandas, NumPy)Data cleaning, transformation, feature engineeringMatplotlib / SeabornExploratory data visualizationPostgreSQLRelational database & analytical queryingSQLAlchemyPython–PostgreSQL pipelinePower BIInteractive business dashboard

## ⚙️ Data Pipeline
Raw CSV
   ↓
Python (Pandas) — Cleaning & Feature Engineering
   ↓
PostgreSQL — Loaded via SQLAlchemy
   ↓
SQL Queries — Business Analysis (10 Questions)
   ↓
Power BI — Interactive Dashboard
Key Preprocessing Steps

Imputed missing Review Rating values using category-level median to avoid bias
Standardized all column names to snake_case
Engineered age_group feature using quartile-based binning → Young Adult, Adult, Middle Aged, Senior
Mapped frequency_of_purchases text to numeric purchase_frequency_days
Removed redundant promo_code_used column (100% identical to discount_applied)


## 🔍 SQL Analysis — 10 Business Questions
<img width="481" height="265" alt="image" src="https://github.com/user-attachments/assets/12750a4f-e7cc-48bf-8a2d-b837d0349b2b" />

## 📊 Dashboard Highlights
<img width="1350" height="737" alt="image" src="https://github.com/user-attachments/assets/3f0a2338-eb3a-4967-b994-2a63767ddd18" />

The Power BI dashboard features interactive filters for Subscription Status, Gender, Category, and Shipping Type, with the following KPIs and visuals:

3.9K Total Customers  |  $59.76 Avg Purchase Amount  |  3.75 Avg Review Rating
🍩 Customers by Subscription Status (73% No / 27% Yes)
📊 Revenue by Category — Clothing leads significantly
📈 Customer Sales by Category — Area trend chart
📉 Revenue & Previous Purchases by Age Group — Young Adults top both


## 💡 Key Business Insights
Revenue & Demographics

Young Adults and Middle-Aged customers are the top revenue-generating segments
Clothing is the dominant category, creating a concentration risk

Discount Strategy

A significant subset of discount users still spend above the $59.76 average — a prime upsell opportunity
Several products show high discount dependency, flagging a need for pricing strategy review

Customer Loyalty

73% of customers are non-subscribers — a massive untapped retention opportunity
Subscribed customers demonstrate higher average and total spend
Customers with 10+ previous purchases are far more likely to be subscribers, confirming that repeat behavior drives subscription conversion

Product Intelligence

Top-rated products identified for hero product marketing campaigns
Per-category product rankings guide inventory prioritization

## 📈 Business Recommendations

Launch a targeted subscription conversion campaign for non-subscribers with 5+ purchases — they are behaviorally ready
Protect high-rated products from over-discounting — use them as anchor products instead
Personalize marketing by age group — Young Adults respond to trend-driven messaging; Seniors may value reliability and service
Double down on Clothing while building campaigns to lift Outerwear and Footwear revenue
Reward high-frequency buyers with early access or exclusive perks to accelerate loyalty
