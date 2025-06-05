# **Mobile Sales Dashboard - Power BI Project**  
**📊 Overview**  
This Power BI project analyzes mobile sales data to provide actionable insights into sales performance, customer behavior, and product trends. The dashboard includes visualizations for revenue, sales trends, top-selling products, and regional performance.  

---

## **📂 Project Structure**  
```
Mobile-Sales-PowerBI/  
├── Data/  
│   ├── mobile_sales_data.xlsx (or .csv)  
│   └── (any additional datasets)  
├── PowerBI/  
│   ├── Mobile_Sales_Dashboard.pbix  
│   └── (supporting files)  
├── Documentation/  
│   ├── Data_Dictionary.md  
│   └── Business_Requirements.md  
└── README.md  
```  

---

## **🔧 Setup & Requirements**  
### **1. Prerequisites**  
- **Power BI Desktop** (Download [here](https://powerbi.microsoft.com/desktop/))  
- Sample dataset (`mobile_sales_data.xlsx` included in `/Data`)  
- Basic knowledge of Power BI (DAX, transformations, visualizations)  

### **2. Data Source**  
- **Primary Dataset**: `mobile_sales_data.xlsx`  
  - Columns: `OrderID`, `Date`, `Product`, `Brand`, `Region`, `Quantity`, `UnitPrice`, `TotalRevenue`, etc.  
- **Data Refresh**:  
  - Direct connection to Excel/CSV (manual refresh).  
  - For automated refreshes, connect to a SQL/API source.  

### **3. Steps to Use**  
1. **Open Power BI Desktop** → Click **"Get Data"** → Select `mobile_sales_data.xlsx`.  
2. **Transform & Clean Data** (if needed) using Power Query.  
3. **Create Relationships** between tables (if multiple datasets).  
4. **Build Visualizations**:  
   - Sales Trends (Line Chart)  
   - Revenue by Brand (Bar Chart)  
   - Top 5 Products (Table)  
   - Regional Sales (Map)  
5. **Save & Publish** to Power BI Service (optional).  

---

## **📊 Dashboard Features**  
### **1. Key Metrics**  
- **Total Revenue**  
- **Units Sold**  
- **Avg. Selling Price**  
- **YoY Growth %**  

### **2. Interactive Visualizations**  
- **Sales Over Time** (Line Chart)  
- **Revenue by Brand** (Stacked Column Chart)  
- **Geographic Sales** (Map)  
- **Product Performance** (Treemap)  

### **3. Filters**  
- Date Range  
- Brand  
- Region  

---

## **📈 Sample DAX Measures**  
```dax
Total Revenue = SUM(mobile_sales[TotalRevenue])  
YoY Growth = 
VAR CurrentYearRevenue = [Total Revenue]  
VAR PreviousYearRevenue = CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(mobile_sales[Date]))  
RETURN DIVIDE((CurrentYearRevenue - PreviousYearRevenue), PreviousYearRevenue)  
```

---

## **🚀 How to Improve This Project?**  
1. **Add More Data Sources**:  
   - Customer demographics  
   - Competitor pricing  
2. **Advanced Analytics**:  
   - Forecasting (Power BI’s built-in AI)  
   - Customer segmentation (RFM analysis)  
3. **Automate Data Refresh**:  
   - Connect to a cloud database (SQL Server, Snowflake).  

---

## **📜 License**  
MIT License. Free to use and modify.  

---

**🔗 Connect**  
- [GitHub](https://github.com/yourusername) | [LinkedIn](https://linkedin.com/in/yourprofile)  

**📧 Contact**  
For questions, email: `your.email@example.com`  

--- 

Happy analyzing! 📱💡
