# 🛒 Quick Commerce India — Market & Performance Analysis

**Advanced Python / Data Analysis — Final Project**  
**Author:** Nandhu Krishnan Radhakrishnan  
**Date:** January 2026

---

## 📋 Overview

This project analyzes a synthetic dataset of **1,000,000 orders** from major quick commerce platforms in India (Swiggy Instamart, Blinkit, Zepto, BigBasket, Dunzo, Amazon Now, Flipkart Minutes, and Jio Mart). The goal is to uncover revenue patterns, customer preferences, and the impact of delivery time and discounts on platform performance.

---

## ❓ Business Questions

1. Which quick commerce platform has the **highest total revenue**?
2. Which platform has the highest **Average Order Value (AOV)**?
3. How does **Customer Rating** vary across platforms?
4. Does **Delivery Time** affect **Delivery Partner Ratings**?
5. What is the most popular **Product Category** on Swiggy Instamart for users aged 20–30 in Mumbai?
6. Are **discounts** increasing order volume or just reducing revenue?

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `RADHAKRISHNAN_NandhuKrishnan_FinalProject.ipynb` | Jupyter Notebook with full analysis and visualizations |
| `RADHAKRISHNAN_NandhuKrishnan_FinalProject.pdf` | Rendered PDF report |

> **Note:** The dataset `quick_commerce_data_raw.csv` is synthetic and not included in this repository due to file size (~100MB). See the Data section below for details.

---

## 📊 Dataset

- **Type:** Synthetic generated data
- **Size:** 1,000,000 rows × 13 columns
- **After cleaning:** 948,000 rows retained

| Column | Description |
|--------|-------------|
| `Order_ID` | Unique order identifier |
| `Company` | Quick commerce platform name |
| `City` | Delivery city |
| `Customer_Age` | Age of the customer (18–59) |
| `Order_Value` | Order amount in INR |
| `Delivery_Time_Min` | Delivery time in minutes |
| `Distance_Km` | Delivery distance in km |
| `Items_Count` | Number of items ordered |
| `Product_Category` | Category of ordered products |
| `Payment_Method` | Payment method used |
| `Customer_Rating` | Customer rating (1–5) |
| `Discount_Applied` | Whether a discount was applied (0/1) |
| `Delivery_Partner_Rating` | Rating for the delivery partner (1–5) |

---

## 🔍 Key Findings

| Question | Finding |
|----------|---------|
| Highest Revenue | **Swiggy Instamart** (₹76.5M total) |
| Highest AOV | **Swiggy Instamart** (₹645.7 avg order) |
| Best Customer Ratings | **Blinkit** (avg 3.58 / 5) |
| Delivery Time vs Rating | **No significant correlation** (r = -0.0028) |
| Top Category (Mumbai, 20–30 yo) | **Household items** |
| Discount Impact | Discounts **increase both** order volume and revenue (AOV ~2× higher with discount) |

---

## 🛠️ Tools & Libraries

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, and manipulation |
| `numpy` | Numerical operations and rounding |
| `matplotlib` | Static visualizations (bar, line, stem, boxplot) |
| `seaborn` | Enhanced statistical plots |
| `plotly.express` | Interactive visualizations |

---

## 🧹 Data Cleaning Steps

1. Dropped rows with missing `City` values (52,000 rows removed)
2. Filled missing `Items_Count` with column mean
3. Filled missing `Customer_Rating` with company-level group mean
4. Filled missing `Delivery_Partner_Rating` with delivery-time group mean, then overall mean for remaining nulls
5. Capped `Order_Value` outliers at ₹2,500 using percentile clipping
6. Converted float columns to integers after rounding
7. Changed `Order_ID` dtype from int to string

---

## 📈 Visualizations Included

- Bar + Line chart: Total revenue by platform
- Stem chart: Average order value by platform
- Boxplot: Customer rating distribution across platforms
- Grouped bar chart: Rating distribution (1–5 stars) per company
- Line chart: Delivery time vs. delivery partner rating
- Horizontal bar chart: Top product categories (filtered segment)
- Subplots: Discount impact on order value and item count

---

## ▶️ How to Run

1. Clone this repository
2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly
   ```
3. Place the dataset file `quick_commerce_data_raw.csv` in the same directory
4. Open the notebook:
   ```bash
   jupyter notebook RADHAKRISHNAN_NandhuKrishnan_FinalProject.ipynb
   ```
5. Run all cells from top to bottom

---

## ⚠️ Limitations

- Dataset is **synthetic** — findings may not reflect real-world market conditions
- Discount analysis shows correlation, not causation
- City-level analysis limited to major metros only
- Delivery time correlation is near zero, possibly due to context-dependent expectations

---

## 🤖 AI Usage

AI was used for interpreting analytical results, generating syntax for outlier removal, and assisting with data cleaning logic.

---

## 📄 License

This project was submitted for academic purposes. The dataset used is synthetically generated and does not represent any real company's proprietary data.
