# **Revenue Generators Dashboard**

![Revenue Generators Dashboard](/Images/Revenue_Generators_Dashboard.gif)


## **Project Overview**
The **Revenue Generators Dashboard** explores BMW’s sales data from 2010–2024 to identify which vehicle configurations and models drive the brand’s overall profitability. It highlights two contrasting yet crucial groups:
- **High-end earners / Outliers** — luxury configurations with exceptional revenue per unit.
- **Top 5% modest revenue generators** — models with moderate unit prices but exceptionally high sales volumes, contributing significantly to total revenue.


### **Dashboard File**
⬇️ Final Dashboard is available here: 

[Revenue Generators Dashboard](/2_Revenue_Generators_Dashboard\Revenue_Generators_Dashboard.xlsx)

### **ℹ️ BMW Sales Data (2010-2014) Dataset**
This dataset was sourced from Kaggle. It appears to represent real-world car sales, but the exact origin or authenticity of the data is not specified. 
It contains following car sales information:
- **Car model, color & transmission type**
- **Production year & sales region**
- **Fuel type, engine size (in liters) & mileage (in kilometers)**
- **Price (in USD) & sales volume**

### **Excel Skills Used**

The following Excel skills were utilized for analysis:

- **🛠️ Power Query**
- **🧮 Formulas and Functions**
- **📅 Pivot Tables**
- **📉 PivotChart**


## **Dashboard Build**

### **🛠️ Power Query (ETL)**

#### **📥 Extract**
- I have used original dataset with changed name (bmw_global_sales) in Power Query to create two more queries: 
    - **top_outliers_models:**  listing top 25 percentile of model configurations in the upper price range that bring high revenues despite lower sales volume
    - **central_50%_configs:** listing model configurations that make 50% of data by high revenue and high sales volume

        ![Queries](/Images/queries.png)   

#### **🔄 Transform**
- Each **query** was transformed by removing unnecessary columns, reordering columns, sorting rows, changing data types and renaming data for simplicity and clarity
- Columns added:
    - **Sales_Total_USD** - total earnings per model configuration
    - **Index & Percentile** - to identify interquartile ranges of the data
    - **Share_of_Core** - to identify top 5% of modest revenue generators
    - **Engine_Size_Category** - to differentiate engines less than and greater than 2.0 Liters

    ![Columns Added](/Images/new_cols(rgd).png)   

#### **🔗 Load**
- All three transformed queries were loaded into the workbook, setting the foundation for subsequent analysis.

### **🧮 Formulas & Functions**
- Calculated metrics:
    - **Sales_Total_USD** = [Price_USD] * [Sales_Volume]
    - **Percentile** = [Index] / #"Counted Rows"
    - **Share_of_Core** = [Sales_Total_USD] / List.Sum(#"Reordered Columns"[Sales_Total_USD])
- Applied conditional logic for categorization

### **📅 Pivot Tables**
- Sorted and filtered data dynamically for top models, engine sizes, and regions
- Aggregated metrics such as total sales and share of core for dashboard insights

### **📉 PivotChart**

- **Column Charts:** Multi-level grouping for models, engine size, fuel type and region for comparison, sorted in descending order by best performing models
- **Line Charts:** Trend analysis for selected model configurations from year 2010 to 2024 
- **Slicers:** Dynamic filtering by model to explore in detail yearly trends

    ![PivotCharts](/Images/charts.png)

## **💡 Dashboard Content and Insights**

- **Outlier Revenue Analysis:** 
    - Visual comparison of top-performing luxury configurations versus high-volume earners
    - *A small cluster of luxury models drives a disproportionate share of premium revenue*
- **Top 5% Modest Revenue Generators:** 
    - Breakdown of models with strong unit sales and consistent contribution to total revenue
    - *The bulk of total revenue originates from modest model configurations priced in the mid-to-high range but sold in large volumes*
- **Yearly Revenue Trend:** 
    - Time-series chart displaying changes in overall revenue and the performance balance between outliers and high-volume models
    - *Revenue concentration shifts slightly year to year, indicating evolving consumer preferences and model line success*
- **Model Configuration View:** 
    - Enables comparison between performance categories



## **Conclusion**
This dashboard demonstrates the ability to combine **data-driven segmentation** and **trend visualization** to uncover what truly drives revenue in a global automotive dataset. It highlights strategic insights relevant to pricing, sales mix, and performance optimization — key skills for business analytics and data visualization roles.
