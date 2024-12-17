# **Sales Data Analysis Project**

## **Project Overview**
This project analyzes **sales data** for 50 weeks. The goal is to identify trends, sudden changes in daily sales, and patterns across different time periods of the day (dayparts). The project includes statistical testing, visualization, and insights extraction.

This project was taken from **StrataScratch** and was part of an **interview process** for a company.

---

## **Dataset Description**
The dataset consists of 50 CSV files (one file per week), each containing:
- `sale_time`: A timestamp indicating when the sale occurred (e.g., `2012-10-01 01:42:22`).
- `purchaser_gender`: Gender of the customer who made the purchase (`male` or `female`).

---

## **Questions Answered**
1. **Daily Sales Trends**:
   - Plot daily sales over 50 weeks.
   - Identify the date with a sudden change in daily sales.

2. **Statistical Significance of Sales Change**:
   - Perform a two-sample t-test to determine if the change is statistically significant.
   - Report the t-statistic and p-value.

3. **Gender Distribution Analysis**:
   - Analyze the proportion of sales made by male and female customers **before** and **after** the sudden change.

4. **Sales by Daypart**:
   - Divide a day into 4 dayparts:
     - **Night**: 12:00 AM - 6:00 AM  
     - **Morning**: 6:00 AM - 12:00 PM  
     - **Afternoon**: 12:00 PM - 6:00 PM  
     - **Evening**: 6:00 PM - 12:00 AM  
   - Calculate the percentage of sales in each daypart.
   - Visualize the results.

---

## **Code and Analysis Steps**

### **1. Importing Libraries and Data**
- All CSV files are dynamically loaded and concatenated into a single DataFrame.

### **2. Analyzing Daily Sales**
- Daily sales are calculated by grouping the data by date.
- A line chart is plotted to visualize trends over time.

### **3. Identifying and Testing Sudden Changes**
- Daily sales differences are calculated to find significant changes.
- A **two-sample t-test** is performed:
   - Null Hypothesis (H₀): There is no difference in daily sales before and after the sudden change.
   - Output: **t-statistic** and **p-value**.

### **4. Gender Distribution Analysis**
- Sales proportions by gender are calculated and visualized using a bar chart.
- Proportions are compared **before** and **after** the sudden change.

### **5. Daypart Analysis**
- Sales are categorized into 4 dayparts based on the sale time.
- The percentage of sales in each daypart is calculated and visualized with a bar chart.
- Value labels are added to enhance readability.

---

## **Key Visualizations**
1. **Daily Sales Line Chart**: Visualizes trends over 50 weeks and highlights sudden changes.
2. **Gender Distribution Bar Charts**: Compare proportions of male and female sales before and after the sudden change.
3. **Daypart Sales Bar Chart**: Displays the percentage of sales in each daypart with clean labels.

---

## **Dependencies**
Ensure the following Python libraries are installed:
```bash
pip install pandas matplotlib scipy
```

---

## **Usage**
1. Place all CSV files in a folder named `datasets` in the same directory as the script.
2. Run the analysis script to load and process the data.
3. Visualizations and statistical outputs will be displayed in the terminal and as plots.

---

## **Sample Outputs**
- Sudden change in sales occurs on **October 10, 2012**.
- The change is statistically significant with a **p-value ≈ 0**.
- Sales by daypart are distributed as follows:
   - **Afternoon**: 39.46%  
   - **Morning**: 30.60%  
   - **Evening**: 20.97%  
   - **Night**: 8.97%  

---

## **Conclusion**
This project provides actionable insights into daily sales trends, customer behavior by gender, and sales distribution across dayparts. The statistical testing validates the significance of observed changes.

---