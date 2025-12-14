# ☕ Café Sales Data Cleaning & Exploratory Data Analysis (EDA)

This project demonstrates a **complete data cleaning and exploratory data analysis (EDA) pipeline** using a **real-world, messy café sales dataset** sourced from Kaggle.

The dataset contains **10,000 transaction records** with significant missing values, invalid entries, and inconsistent data types — making it ideal for showcasing **practical data cleaning, feature engineering, and analytical thinking**.

---

## 📌 Dataset Overview

**Raw Dataset Characteristics:**
- 10,000 transaction records
- All columns initially stored as `object` type
- High missingness in categorical columns:
  - Payment Method (~25% missing)
  - Location (~33% missing)
- Invalid placeholders such as `"ERROR"` and `"UNKNOWN"`
- Numeric values stored as strings

**Columns:**
- Transaction ID  
- Item  
- Quantity  
- Price Per Unit  
- Total Spent  
- Payment Method  
- Location  
- Transaction Date  

---

## 🎯 Project Objective

To transform raw café transaction data into **clean, structured, and analyzable data**, and extract **business-relevant insights** using:

- **Univariate analysis**
- **Bivariate analysis**
- **Multivariate analysis**

---

## 🧹 Part 1: Data Cleaning

The following steps were performed to prepare the dataset for analysis:

### 🔹 Data Quality Improvements
- Replaced invalid values (`"ERROR"`, `"UNKNOWN"`) with proper nulls
- Converted numeric columns:
  - Quantity
  - Price Per Unit
  - Total Spent
- Used **median imputation** for numeric columns to preserve distribution
- Filled categorical missing values using:
  - Mode (Item, Payment Method)
  - Contextual placeholder (`"Unknown"` for Location)

### 🔹 Date Processing & Feature Engineering
- Converted `Transaction Date` to datetime
- Filled missing dates using the **median date**
- Engineered new features:
  - Day of Week
  - Month
  - Year
  - Item Revenue (`Price Per Unit × Quantity`)

### 🔹 Final Checks
- Removed duplicate records
- Verified data types and null values
- Exported cleaned dataset as `cafe_sales_cleaned.csv`

---

## 📊 Part 2: Exploratory Data Analysis (EDA)

EDA is structured into **Sales Insights**, **Time-Based Patterns**, and **Customer Behavior**, with each visualization clearly categorized as **Univariate, Bivariate, or Multivariate**.

---

## 🔹 1. Sales Insights

### 1.1 Most Frequently Sold Items  
**(Univariate Analysis)**  
- Bar chart of item frequency  
- Identifies high-demand products for inventory planning  

### 1.2 Highest Revenue-Generating Items  
**(Univariate Analysis)**  
- Revenue-based ranking using `Item Revenue`  
- Bar chart and pie chart visualization  
- Highlights the café’s most profitable items  

### 1.3 Quantity vs Total Spend Relationship  
**(Bivariate Analysis)**  
- Scatter plot: Quantity vs Total Spent  
- Reveals items with high revenue despite lower quantities  

---

## 🔹 2. Time-Based Patterns

### 2.1 Sales by Day of the Week  
**(Univariate Analysis)**  
- Total revenue by weekday  
- Helps optimize staffing and promotions  

### 2.2 Monthly Sales Trends  
**(Univariate Analysis)**  
- Revenue comparison across months  
- Identifies seasonality and demand shifts  

### 2.3 Payment Preference: Weekday vs Weekend  
**(Bivariate Analysis)**  
- Heatmap of Day vs Payment Method  
- Shows behavioral differences in payment usage  

### 2.4 Monthly Sales by Payment Method  
**(Multivariate Analysis)**  
- Line plot: Month × Payment Method × Total Sales  
- Identifies which payment methods drive growth over time  

---

## 🔹 3. Customer Behavior

### 3.1 Most Common Payment Methods  
**(Univariate Analysis)**  
- Frequency distribution of payment types  

### 3.2 Average Spend by Payment Method  
**(Bivariate Analysis)**  
- Comparison of average transaction values  
- Highlights spending behavior differences  

### 3.3 Spend by Location and Payment Type  
**(Bivariate Analysis)**  
- In-store vs Takeaway spending patterns  

### 3.4 Top Items Across Months & Payment Types  
**(Multivariate Analysis)**  
- FacetGrid visualization  
- Combines Item, Month, Payment Method, and Revenue  
- Reveals seasonal and payment-based performance trends  

---

## 🔹 4. Cross-Thematic Multivariate Insight

### Highest Average Transaction Value Combination

**Question:**  
Which combination of **Day of Week, Location, and Payment Method** yields the highest average transaction value?

**Analysis Type:** Multivariate  

- Heatmap visualization  
- Identifies high-value customer segments  
- Supports data-driven business decisions  

---

## 📁 Repository Structure

| File | Description |
|----|------------|
| `Cafe_Sales_Data_Cleaning_&_EDA.ipynb` | Complete notebook with cleaning, EDA, and visualizations |
| `cafe_sales_dirty.csv` | Original raw dataset |
| `cafe_sales_cleaned.csv` | Cleaned dataset generated during analysis |

---

## ▶️ How to Run the Notebook

### Run Using **VS Code**

1. Install **Python (3.8 or higher)**
2. Install **Visual Studio Code**
3. Install VS Code extensions:
   - Python
   - Jupyter
4. Clone or download this repository
5. Open the project folder in VS Code
6. Ensure all `.csv` files are in the same directory as the notebook
7. Open `Cafe_Sales_Data_Cleaning_&_EDA.ipynb`
8. Select a Python kernel
9. Click **Run All** or execute cells sequentially

---

### Run Using **Google Colab**

1. Open Google Colab
2. Upload the `.ipynb` file
3. Upload the `.csv` files
4. Run all cells from top to bottom

---

## 🛠️ Tools & Technologies

- Python
  - Pandas
  - Matplotlib
  - Seaborn
- Jupyter Notebook
- Google Colab
- VS Code

---

## ✅ Project Status

✔ Project Completed  
💬 Open to feedback and suggestions
