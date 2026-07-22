# 📊 Overcoming Profit Leakage from Aggressive Discounting Strategy

## 📌 Project Overview
This project analyzes retail transaction data from the Superstore dataset to identify **profit leakage caused by aggressive discount strategies**.

The analysis focuses on uncovering cases where **high sales do not translate into high profit**, evaluating the relationship between **discount and profit margin**, and identifying **regions and product categories contributing to losses**.

The goal is to provide actionable insights to improve pricing strategies and prevent margin erosion.

---

## 🎯 Problem Statement
In a highly competitive market, companies often fall into a **growth trap**—focusing on increasing revenue while neglecting profitability.

According to McKinsey, poor pricing and uncontrolled discount strategies can reduce profitability by **20–30%**, even when sales are increasing.

This project aims to evaluate whether discount strategies are negatively impacting profit performance in the Superstore dataset.

---

## 🛠️ Tools & Technologies
- Python  
- Pandas  
- Jupyter Notebook (VS Code)  

---

## ❓ Business Questions
- Are there cases where **high sales generate low profit**?  
- How does **discount impact profit margin**?  
- Which **regions or segments contribute most to losses**?  

---

## 📊 Dataset Information
- Dataset: Superstore  
- Source: Kaggle  
- Rows: 9,994  
- Columns: 21  
- Format: CSV  

---

## 🧹 Data Preparation Process

### Data Cleaning
- Corrected data types:
  - `Order Date` → datetime  
  - `Ship Date` → datetime  
- Renamed columns (removed spaces for better querying)

### Data Validation
- No missing values  
- No duplicate records  
- Outliers retained (represent real business transactions)

### Statistical Findings
- `Sales`: highly right-skewed  
- `Quantity`: mostly between 2–3  
- `Discount`: mostly between 0–20%  
- `Profit`: includes negative values (loss transactions)

### Feature Engineering
- `unit_price` → price before discount  
- `profit_margin` → profit-to-sales ratio  

---

## 📈 Key Insights

### 1. High Sales ≠ High Profit (Machines Sub-Category)
The **Machines** sub-category shows strong sales but extremely low profit:

- Sales: ~$189K (112 orders)  
- Profit: ~$3.38K  

Compared to Copiers:
- Lower sales (~$149K)  
- Much higher profit (~$55K)  

➡️ Problem lies in **margin, not volume**

---

### 2. Massive Loss Contribution
- 47.34% of Machine transactions are unprofitable  
- Total loss: ~$30,118  

➡️ Loss transactions significantly erode total profit

---

### 3. Strong Negative Impact of Discounts
There is a clear **negative relationship** between discount and profit margin:

- Higher discount → lower margin  
- Most losses occur at **40%–70% discount levels**

#### Example Case
- Normal price: $20,993  
- Discount: 70%  
- Final sales: $6,299  
- Loss: $9,239  
- Profit margin: -147%  

➡️ Aggressive discounting destroys profitability

---

### 4. Regional Loss Concentration (Ohio)
- Largest loss contributor: **Ohio**
  - Total loss: ~$11,770  
  - 8 customers  
  - High AOV (~$1,200)

➡️ Indicates pricing or contract issues in this region

---

### 5. Category-Level Performance Imbalance
- Office Supplies → highest order volume  
- Technology → highest profit  
- Furniture → very low profit  

➡️ Not all categories contribute equally to profitability

---

## 🧠 Conclusion
The Machines sub-category is a clear example of a **growth trap**, where high sales volume does not translate into profitability.

The main issue is **uncontrolled discounting**, leading to significant cumulative losses and margin erosion.

---

## 💡 Recommendations

### 1. Implement Discount Cap
- Limit discounts to **maximum 40%**
- Prevent margin from dropping into negative territory  

---

### 2. Evaluate Ohio Market Strategy
- Audit pricing and contracts for key customers  
- Replace discount strategy with:
  - Extended warranty  
  - Service bundles  

---

### 3. Review High-Risk Products
- Evaluate products with high sensitivity to discount  
- Consider:
  - Increasing base price  
  - Limiting sales volume  
  - Removing unprofitable items  

---

## 🚀 Final Note
This analysis highlights that **revenue growth alone is not enough**—sustainable business performance depends on maintaining **healthy profit margins through controlled pricing strategies**.
