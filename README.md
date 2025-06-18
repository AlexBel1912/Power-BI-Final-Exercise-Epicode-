# 📊 Olist E-commerce Analysis – Power BI Interactive Dashboard

## 🛒 About the Project

This project presents a comprehensive **Business Intelligence report** developed in **Power BI** as the final assignment for the **Power BI module at Epicode**. Using the **public Olist dataset** (Brazilian e-commerce platform), the report provides strategic and dynamic insights into the platform's commercial evolution between **2016 and 2018**.

### Project Scenario
Olist Store is a Brazilian e-commerce platform that connects sellers to diverse Brazilian markets. This analysis explores the **public anonymized dataset** containing sales orders from 2016 to 2018, enabling comprehensive measurement and analysis across multiple dimensions: customers, products, payment methods, order status, and geographic distribution.

## 🎯 Analysis Objectives

This BI report was designed to answer the following key business questions:

1. **Order Trends Over Time by State**: Month-by-month order analysis with year-over-year comparisons and percentage variations, filterable by order status
2. **Revenue Evolution by State**: Monthly revenue trends with previous year comparisons and YoY growth analysis
3. **Customer Review Distribution**: Analysis of rating patterns to assess service quality and customer satisfaction

### Additional Features
- Enable filtering by **order status**, **state**, and **year**
- Provide **narrative insights** and **interactive storytelling**
- Implement drill-throughs and dynamic tooltips for advanced analysis
- Geographic analysis with Brazilian state-level performance metrics
- Delivery performance tracking and categorization

## 🧩 Data Model & Transformation

### Power Query Transformations
- **Data Cleaning**: Removed null values, duplicates, and inconsistent data entries
- **Column Optimization**: Eliminated unnecessary columns to improve model performance
- **Data Transformation**: Standardized data types, formats, and naming conventions
- **Table Merging**: Combined relevant tables for comprehensive cross-dimensional analysis
- **Products**: Translated product categories from Portuguese to English for accessibility
- **Geographic Data Cleaning**: Validated and standardized Brazilian state and city information

### Star Schema Structure
- **Fact Table**: `Orders` (central fact table containing order transactions)
- **Dimension Tables**: `Customers`, `Items`, `Products`, `Reviews`, `Payments`, `d_Calendar`
- **Custom Calendar Table**: `d_Calendar` created to support all time intelligence measures (YTD, PY, YoY%)

### Tables Used
- `olist_orders_dataset`
- `olist_order_items_dataset` 
- `olist_products_dataset`
- `olist_order_reviews_dataset`
- `olist_customers_dataset`

*Note: `olist_geolocation_dataset` was cleaned in Power Query, and `olist_sellers_dataset` was excluded from the final model.*

## 💡 Key DAX Measures Implemented

### Revenue Measures
- **Total Sales**: Sums ALL orders, ignoring filters
- **Sales**: Revenue with applied filters (price + freight_value)
- **Sales PY**: Previous year sales for comparison
- **Sales PY %**: Year-over-year percentage variation
- **Sales YTD**: Cumulative revenue from beginning of year

### Order Measures
- **Orders**: Current period order count
- **Orders PY**: Previous year orders for same period
- **Orders PY %**: Year-over-year order variation
- **Orders YTD**: Cumulative orders from start of year

### Customer & Review Measures
- **Average Reviews**: Customer satisfaction score with filters
- **Average Reviews Remove Filt**: Global average (no filters)
- **AOV (Average Order Value)**: (price + freight_value) / distinct orders

### Delivery Performance Metrics
- **DaysPassed**: Days between order date and delivery date
- **DeliveryRange**: Classification system:
  - **In Time** (≤ 20 days)
  - **Acceptable** (21–50 days)
  - **Delay** (> 50 days)
  - **No Data** (missing delivery information)

## 📍 Report Pages & Features

### 🏠 Overview Dashboard
- **KPI Cards**: Total Orders (99,441), Revenue (R$15.84M), Average Review (4.09), Unique Customers (96,096)
- **Navigation Hub**: Central buttons for seamless page transitions
- **Dynamic Filters**: Year selection, state filtering, order status controls

### 📈 Orders Analysis
- Monthly order trends with previous year comparisons
- YoY percentage changes visualization
- Interactive time-series charts

### 💸 Sales Analysis  
- Monthly revenue breakdown and trends
- Year-over-year growth analysis
- Revenue performance by state

### 🌍 Geographic Analysis
- **Interactive map** of Brazilian states
- State-level performance metrics
- Top 10 locations by orders and sales
- Drill-through capabilities for location-specific insights

### ⭐ Customer Reviews
- Review score distribution analysis
- **57.78%** five-star reviews indicating high satisfaction
- Correlation analysis between delivery performance and ratings

### 🚚 Delivery Performance
- **83.80%** on-time delivery rate
- Performance categorization and trend analysis
- Cross-analysis with customer satisfaction scores

## 🛠 Tools & Technologies Used

- **Power BI Desktop** - Main dashboard development and visualization
- **Power Query** - Used for cleaning and transforming raw datasets.
- **DAX** - Custom measures and advanced calculations
- **Excel** - For Data Validation

## 📦 Dataset Source

[Brazilian E-Commerce Public Dataset by Olist] Provided by Epicode for educational purposes
This dataset contains anonymized orders made at Olist Store from 2016 to 2018.

## 🔍 Key Business Insights

### Three-Year Evolution Pattern
- **2016 (Foundation)**: 329 total orders, experimental phase with R$57K revenue
- **2017 (Growth)**: Steady expansion reaching R$7.1M total revenue
- **2018 (Maturity)**: 54,011 orders with consistent R$1M+ monthly revenue

### Geographic Performance
- **São Paulo** dominates with **44.20%** of total orders
- **Rio de Janeiro** accounts for **12.17%** of order volume
- **Top product categories**: Health & Beauty, Bed Bath Table, Sports Leisure

### Operational Excellence
- **83.80%** on-time delivery performance
- **4.09/5** average customer satisfaction score
- **120.05%** year-over-year sales growth rate

## 🚀 How to Use This Report

1. Download the `.pbix` file from this repository
2. Open with Power BI Desktop (latest version recommended)
3. Use the **year slicers** to focus on specific time periods
4. Apply **state and order status filters** for targeted analysis
5. Navigate between pages using the central **navigation buttons**
6. Explore the **Geographic Analysis** page for detailed regional insights
7. Use the **"Clear all slicers"** button to reset filters and start fresh

### Navigation Tips
- Start with the **Overview Dashboard** for high-level KPIs
- Check **narrative panels** for automated insights
- Hover over visuals for detailed **interactive tooltips**

📁 Repository Structure

📦 Repository Root
├── 📁 file csv # data files for analysis
├── 📁 images/ # Icons and visual assets
│   └── 🖼️ [various icons used in reports]
├── 📁 sample report # Power BI dashboard
├── 📄 W20D4 - Final Exercise.pbix # Power BI project file
└── 📄 W20D4 - Final Exercise Report.pdf # Complete project report


## 🎓 Academic Context

This project was developed as the **final exercise assignment** for the **Power BI module** in the **Data Analytics program at Epicode**. The analysis demonstrates proficiency in:

- **Star schema** data modeling
- **Advanced DAX** calculations and time intelligence
- **User Experience (UX)** design for analytical dashboards
- **Data storytelling** and narrative insights

## 👩‍💻 Author

**Alexandra Belacurencu**  
*Data Analyst*

🛠️ **Technical Skills**: Excel | SQL | Python | Power BI | Data Visualization  
🎓 **Education**: Data Analytics Program - Epicode  
🔗 **Connect**: [LinkedIn](https://www.linkedin.com/in/alexandra-belacurencu/)| [GitHub](https://github.com/AlexBel1912) | [Portfolio](https://sites.google.com/view/alexandrabela/progetti)

---

## 📋 Technical Specifications

### System Requirements
- **Power BI Desktop** (March 2023 or later)
- **Minimum RAM**: 4GB (8GB recommended)
- **Operating System**: Windows 10/11

### Performance Optimizations
- **Star schema** implementation for optimal query performance
- **Reduced dataset** through Power Query Cleaning
- **Optimized DAX measures** using variables and performance best practices
- **Efficient relationships** between fact and dimension tables

### Data Refresh
- **Static dataset**: No automatic refresh required
- **Historical analysis**: Covers 2016-2018 period
- **Data source**: Local files (no external connections needed)

---

*This project showcases the practical application of Business Intelligence principles to real-world e-commerce data, demonstrating the power of Power BI for strategic business analysis and decision-making support.*
