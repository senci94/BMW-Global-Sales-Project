# **BMW Sales Dashboard**

![BMW Sales Dashboard](/Images/BMW_Sales_Dashboard.gif)


## **Project Overview**
The **BMW Sales Dashboard** provides an interactive, executive-level overview of BMW’s sales performance between 2010 and 2024. It’s designed for **strategic decision-making** — enabling region and model-level exploration through slicers, while automatically updating key metrics and visuals.

This dashboard focuses on year-over-year growth, powertrain trends (ICE vs xEVs), and pricing dynamics to reveal how BMW’s product mix and market performance evolved over time.


### **Dashboard File**
⬇️ Final Dashboard is available here: 

[BMW Sales Dashboard](/1_BMW_Sales_Dashboard/BMW_Sales_Dashboard.xlsx)

#### **How to Use the Dashboard**
1. Use **region** and **model slicers** to filter all visuals dynamically.
2. Observe **KPI cards** update instantly to reflect selections.
3. Compare **ICE vs xEV trends** and YoY growth to track technological and market evolution.
4. Compare trends and YoY growth in total sale earnings based on **model and region**
5. Review **price range charts** to identify profitability and sales distribution patterns.


### **ℹ️ BMW Sales Data (2010-2014) Dataset**
This dataset was sourced from Kaggle. It appears to represent real-world car sales, but the exact origin or authenticity of the data is not specified. 
It contains following car sales information:
- *Car model, color & transmission type*
- *Production year & sales region*
- *Fuel type, engine size (in liters) & mileage (in kilometers)*
- *Price (in USD) & sales volume*

### **❓Questions to analyze**
1. **How do total and median sales differ across segments?**
2. **Which price range delivers the *highest earnings* and *highest sales volumes*?**
3. **What is the year-over-year (YoY) sales growth rate by region or model?**
4. **How has the ratio of *xEVs to ICE* vehicles evolved over the years?**


### **📝 Excel Skills Used**

The following Excel skills were utilized for analysis:

- **📅 Pivot Tables**
- **📈 Pivot Charts**
- **🔢 Power Pivot & DAX (Data Analysis Expressions)**
- **🛠️ Power Query**

## **1️⃣ How do total and median sales differ across segments?**

*Skills utilized:*

- **🔢 Power Pivot & DAX** -  Measures created for accurate representation of central tendency:

    *Median_Sales_Total_USD=MEDIAN(bmw_global_sales[Sales_Total_USD])*

    *Total_Sales_USD=SUM(bmw_global_sales[Sales_Total_USD])*

- **📅 Pivot Tables** - Linking for dynamic KPI cards for Total Sales and Median Sales, auto-updating with slicer filters.

**💡 Insights:**

The large gap between Total Sales (hundreds of billions) and Median Sales (hundreds of millions) reveals a highly skewed revenue distribution — a few premium BMW models drive a disproportionate share of total global revenue.

However, the global median sales have shown a steady year-over-year increase, suggesting that while outlier models dominate overall earnings, the average-performing models are improving in revenue contribution over time.


 ![Global Median Trend](/Images/median_trends.png)


## **2️⃣ Which price range delivers the *highest earnings* and *highest sales volumes*?**

*Skills utilized:*

- **📅 Pivot Tables** - Aggregate quantity by model and region
- **🛠️ Power Query** - Conditional columns for price segmentation
- **📊 Pie Charts** - Comparing revenue and volume by price category

**💡 Insights:**

Vehicles positioned in the upper-mid segment combine premium pricing with broad market appeal.
This indicates that while ultra-luxury models strengthen brand prestige, the core revenue driver lies in attainable luxury offerings, where customer demand and profitability align most effectively.

 ![Price Analysis](/Images/Price_analysis.png)


## **3️⃣ What is the year-over-year (YoY) growth trend in BMW sales?**

*Skills utilized:*

- **🔢 Power Pivot & DAX** - Compute percentage change in total revenue vs previous year with measures such as:

    ![Total Sales YoY Growth Trend by Region](/Images/yoy_region.gif)
    
- **📅 Pivot Tables** - Aggregation of growth % in total sales year-to-year by region and model
- **📈 Line Charts** - Displaying yearly trends with clearly displayed percentages

**💡 Insights:**

A noticeable sales decline occurred in 2023 across most regions and models, followed by steady growth in 2024.
This reflects a temporary performance dip—possibly due to market disruptions—followed by strong recovery momentum, indicating that key BMW segments regained growth stability post-2023.


## **4️⃣ How has the ratio of xEVs (electric/hybrid) to ICE vehicles evolved over the years?**

*Skills utilized:*

- **🛠️ Power Query** - Conditional columns to categorize models by powertrain type (xEV vs ICE).
- **🔢 Power Pivot & DAX** - Measures showing ratio of YoY growth xEV's to ICE cars

    ![YoY Growth xEv's to ICE](/Images/yoy_xev_ice.gif)

- **📊 Stacked column chart** - Yearly ratios by region

- **📅 Pivot Tables** - Aggregations and percentage calculations


**💡 Insights:**

Across nearly all regions, xEVs achieved slightly higher sales volumes than ICE models, indicating a consistent market shift toward electrification.

Despite fluctuations for xEV's, the overall trajectory is upward, demonstrating growing adoption of electric models and changing consumer demand.

![xEV's vs ICE](/Images/xevs_vs_ice.png)


## **Conclusion**
The BMW Sales Dashboard highlights the ability to design **fully interactive Excel dashboards** that provide meaningful insights for business users. It demonstrates mastery of Excel’s analytical and visualization capabilities — from Power Pivot data modeling to KPI automation and storytelling through clean, professional dashboard design. It is a dynamic display of crucial skills: analytical thinking, attention to data integrity, and the ability to communicate insights visually and effectively.
