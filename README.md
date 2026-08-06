# Costco Global Sales Analysis (2020–2024)

<img width="666" height="375" alt="costco logo (1)" src="https://github.com/user-attachments/assets/b4a106b2-ae1e-485b-a7a2-d033459b2dd9" />

**A 5-year Power BI dashboard analyzing Costco's global sales performance — revenue, profit, regions, and customer segments — built to support real-time, data-driven decision making.**

<img width="756" height="432" alt="Dashboard Overview" src="https://github.com/user-attachments/assets/f25318d5-6429-485a-b9c7-5802d30066b0" />

---

## Project Task

<img width="666" height="375" alt="costco logo (1)" src="https://github.com/user-attachments/assets/feccbade-157f-4388-a4e2-8644cc061e91" />


The goal: analyze the data to uncover which products performed well each year, which categories generated profits or losses, and which regions excelled — then build a real-time dashboard for management to track business progress and make informed decisions.

---

## Dataset

| File | Description |
|---|---|
| `2020.csv` – `2024.csv` | Yearly order-level sales transactions (order ID, dates, ship mode, customer ID, product ID, quantity, discount) |
| `customers.csv` | Customer details — segment, country/city, state, region |
| `products.csv` | Product catalog — category, sub-category, unit price, cost of goods sold |
| `Costco_Sales_Report_2.pbix` | The full Power BI dashboard file |

---

## Tools Used

- **Power BI** — data modeling, dashboard design
- **Power Query** — data cleaning and transformation
- **DAX** — custom KPI measures

---

## Approach

### 1. Data Preparation
- Cleaned and merged 5 years of order data with the customer and product tables using `customer_id` and `product_id`
- Split location data into Country, State, and Region for regional analysis
- Removed duplicates and standardized inconsistent values
<img width="1366" height="733" alt="Power Query View" src="https://github.com/user-attachments/assets/3d4f8151-cc94-4113-9450-de771623ba74" />

### 2. Data Modeling
- Built a star schema: a central fact table (orders) connected to dimension tables for customers, products, and date
- Established clean relationships to support accurate cross-filtering
<img width="976" height="500" alt="ERD Diagram" src="https://github.com/user-attachments/assets/3320eab6-6018-4d45-9407-db021fbf4c31" />

### 3. KPI Development (DAX)
- Built measures for Total Revenue, Total Profit, Quantity Sold, and Year-over-Year growth
- Created Target vs. Actual comparisons for revenue and orders
<img width="280" height="530" alt="Measure 1" src="https://github.com/user-attachments/assets/ae86f46c-816c-4250-af5f-2acf5600834d" />

<img width="280" height="541" alt="Measures 2" src="https://github.com/user-attachments/assets/bdfea8ae-c68a-4995-8fd6-671015fa3188" />

### 4. Dashboard Design
- Interactive slicers for Year, Category, Sub-Category, Region, Quarter, and Ship Mode
- A "Clear All Filters" button for quick resets
- Regional breakdown via map visuals across West, East, Central, and South
- Segment-level drilldowns for Consumer, Corporate, and Home Office customers

---

## Key Features

- **Revenue & Profit Tracking** across all five years, broken down by region and segment
- **Target vs. Actual Performance** to flag where the business is over- or under-shooting goals
- **Product-Level Insights** — a detailed table of revenue, profit, and quantity by product
- **Custom Filter Panel** — toggle open/close, with dedicated icons for filtering and clearing filters
- **Year-over-Year KPIs** — quick visual read on whether revenue, profit, and quantity are trending up or down

---

## Business Value

This dashboard allows Costco's team to:
- Spot top-performing and underperforming regions at a glance
- Understand which customer segments and products drive the most revenue
- Compare actual performance against targets to catch gaps early
- Make faster, self-service decisions without waiting on manual reports

---

##  **Business Problems Solved**

1. **Revenue and Profit Analysis**:
   - Identify top-performing regions and segments to allocate resources effectively.
   - Highlight underperforming areas to strategize improvements.

2. **Customer Segmentation**:
   - Understand customer behavior by segment (Consumer, Corporate, Home Office).
   - Optimize marketing efforts for each customer group.

3. **Product Profitability**:
   - Determine high-revenue products and those with the best profit margins.
   - Align inventory management with product performance.

4. **Target vs. Actual Performance**:
   - Track yearly revenue and order targets.
   - Identify gaps and strategize to meet business goals.

5. **Regional Insights**:
   - Analyze state-level sales to prioritize expansion or cost-cutting measures.
   - Address regional disparities in revenue generation.

6. **Trend Analysis**:
   - Year-over-year comparisons highlight areas of growth and decline.
   - Enable proactive planning based on historical trends.

---

##  **Key Takeaways for Stakeholders**

-  **Executives**: Gain a high-level overview of revenue, profit, and sales trends.
-  **Sales Teams**: Identify opportunities for upselling and improving regional performance.
-  **Analysts**: Drill down into granular data for deeper insights.

---

## **Key Features**

### 1. **Data Preprocessing Using Power Query**
- ✅ Removed duplicates and replaced invalid values with `NULL` to ensure data consistency.
- ✅ Eliminated unnecessary columns to streamline the dataset.
- ✅ Sorted data for better organization.
- ✅ Split customer data into **Country** and **State** columns for enhanced granularity.
- ✅ Merged 5 years of global sales data with the **Products Table** using `product_id` to integrate product pricing.

### 2. **Data Transformation and Calculations**
Using DAX formulas, the following metrics were derived:
- **Net Sale**: Total sales after discounts.
- **Total Revenue**: Revenue generated across all transactions.
- **Total Profit**: Net profit after deducting costs.

### 3. **Comprehensive Visualizations**
- **Summary Metrics**:
  - **Total Revenue**: $2.9M
  - **Total Profit**: $1.6M
  - **Total Quantity Sold**: 49.3K units
- **Revenue and Profit by Region**:
  - Dynamic visuals showing performance in **West, East, Central, and South regions**.
- **Revenue Target vs. Total Revenue**:
  - Compare annual performance against pre-set targets for actionable insights.
- **Orders vs. Target Orders**:
  - Analyze the gap between achieved and target orders.
- **Revenue by Segment**:
  - Contribution by **Consumer**, **Corporate**, and **Home Office** segments.
- **Product-Level Insights**:
  - A detailed table showing **product name, total revenue, target revenue, total profit, total quantity, and total orders**.
- **Shape Map**:
  - A USA map displaying performance by state, aiding in regional analysis.

### 4. **Advanced Filtering Options**
- **Slicers**:
  - Filter data by **Year**.
- **Custom Filter Pane**:
  - Dynamic filters for **Category, Sub-Category, Region, Quarter, and Ship Mode**.
  - Open/Close functionality for a streamlined user experience.
- **Clear All Filters Button**:
  - Reset filters to explore data without constraints.

### 5. **Key Performance Indicators (KPIs)**
- Comparative metrics showing percentage increase or decrease in:
  - **Total Revenue**
  - **Profit**
  - **Quantity Sold**
- KPI highlights year-over-year trends, enabling quick identification of growth or decline.
