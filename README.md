
# 📊 Unit Economics Analysis for TechStream Solutions

Background: Streamline Pro is a comprehensive project management and collaboration tool designed to help businesses manage projects, track progress, and collaborate efficiently. Understanding the unit economics of Streamline Pro is crucial for evaluating its financial health and sustainability. This involves analyzing key metrics such as  **Customer Acquisition Cost (CAC), Average Revenue Per User (ARPU), Cost of Goods Sold (COGS), Gross Margin, Customer Lifetime Value (LTV), and the LTV/CAC ratio.**

***Objective:  Analyze financial efficiency by calculating the unit economics for Streamline Pro for the month of March 2023.***

This project is implemented using **Python, Pandas, and Google Colab** to analyze business profitability and customer acquisition efficiency.

---

## 📊 Key Metrics Explained

| Metric | Description |
|--------|------------|
| **Customer Acquisition Cost (CAC)** | Total cost spent to acquire a new customer. |
| **Average Revenue Per User (ARPU)** | Average revenue earned per customer. |
| **Cost of Goods Sold (COGS)** | Direct costs associated with service delivery. |
| **Gross Margin (%)** | Percentage of revenue remaining after deducting COGS. |
| **Lifetime Value (LTV)** | Total revenue expected from a customer over their lifecycle. |
| **LTV/CAC Ratio** | Measures profitability of customer acquisition. |


---

## 📜 Code Implementation

Below is the core Python code used for the **Unit Economics Analysis**:

### 🔹 Import libraries
```python
import pandas as pd
import numpy as np
```

### 🔹 Create a function for extracting data on March 2023
```python
def read_file_ggsheet(file_id,month_col = None):
  df_ggsheet= pd.read_excel("https://docs.google.com/spreadsheets/d/"+ file_id +"/export?format=xlsx")
  if month_col is not None:
    df_202303 = df_ggsheet[(df_ggsheet[month_col].dt.month == 3) & (df_ggsheet[month_col].dt.year == 2023)]
    return df_202303
  else:
    return df_ggsheet

```

🔍 **Explanation:**
- Manually extracting data from each source is time-consuming and inefficient. To enhance efficiency, a function is implemented to automate the extraction process like the above.

🔍 **Metrics calculation**
After successfully extracting required data, each of these metrics is **calculated in the Google Colab Notebook (`Metric.ipynb`)**.

---

## 📈 Summary of Results & Insights

- **Customer Acquisition Cost (CAC) = $1,092.54**  
  - 🔹 **High acquisition cost**, indicating significant spending on marketing and sales to gain new customers.  

- **Average Revenue Per User (ARPU) = $284.36**  
  - 🔹 No comments.

- **Cost of Goods Sold (COGS) = $22,540**  
  - 🔹 **High operational costs**, can be significantly impacting overall profitability.  

- **Gross Margin = 72.85%**  
  - 🔹 The company retains **72.85% of revenue** after covering direct costs, which is a **strong margin** for a SaaS business.  

- **Lifetime Value (LTV) = $1,930.80**  
  - 🔹No comments.

- **LTV/CAC Ratio = 1.767**  
  - 🔹 Since **LTV/CAC < 3**, the company **is not yet in an optimal profitability range**.  
  - 🔹 **A ratio below 3** suggests the company should either **increase LTV** or **lower CAC** for sustainable growth.  

## 📢 Key Recommendation  
The company should focus on **reducing CAC and increasing ARPU** to improve profitability and efficiency. 🚀


---



