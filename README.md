# 🛍️ Customer Shopping Behavior Analysis

A full end-to-end data analysis project exploring customer shopping patterns, spending habits, product preferences, and subscription behavior using Python, SQL (PostgreSQL), and Power BI.

---

## 📌 Project Overview

This project analyzes **3,900 customer transactions** across multiple product categories to uncover actionable business insights that guide strategic decisions in marketing, product positioning, and customer retention.

---

## 📂 Dataset Summary

| Feature | Details |
|---|---|
| Rows | 3,900 |
| Columns | 18 |
| Missing Data | 37 values in `Review Rating` column |

**Key Feature Groups:**
- **Demographics:** Age, Gender, Location, Subscription Status
- **Purchase Details:** Item, Category, Amount (USD), Season, Size, Color
- **Behavior:** Discount Applied, Promo Code, Previous Purchases, Frequency, Review Rating, Shipping Type

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python (pandas) | Data cleaning & feature engineering |
| PostgreSQL | SQL-based business analysis |
| Power BI | Interactive dashboard |

---

## 🧹 Data Cleaning (Python)

- Loaded dataset with **pandas**
- Imputed 37 missing `Review Rating` values using **median per product category**
- Renamed columns to **snake_case**
- Engineered new columns: `age_group`, `purchase_frequency_days`
- Dropped redundant column `promo_code_used` (duplicate of `discount_applied`)
- Exported cleaned data to **PostgreSQL** for SQL analysis

---

## 🗄️ SQL Analysis (PostgreSQL)

10 business queries were run to answer key questions:

1. **Revenue by Gender** – Male: $157,890 | Female: $75,191
2. **High-Spending Discount Users** – 839 customers used discounts but spent above average
3. **Top 5 Products by Rating** – Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), Skirt (3.78)
4. **Shipping Type Comparison** – Express avg: $60.48 | Standard avg: $58.46
5. **Subscribers vs. Non-Subscribers** – Similar avg spend (~$59), but non-subscribers = 73% of customers
6. **Discount-Dependent Products** – Hat (50%), Sneakers (49.66%), Coat (49.07%), Sweater (48.17%), Pants (47.37%)
7. **Customer Segmentation** – Loyal: 3,116 | Returning: 701 | New: 83
8. **Top 3 Products per Category** – Jewelry, Blouse, Sandals, Jacket lead their categories
9. **Repeat Buyers & Subscriptions** – 2,518 repeat buyers are non-subscribers vs. 958 subscribers
10. **Revenue by Age Group** – Young Adult: $62,143 | Middle-aged: $59,197 | Adult: $55,978 | Senior: $55,763

---

## 📊 Power BI Dashboard

An interactive dashboard was built with the following KPIs and visuals:

- **3.9K** Total Customers
- **$59.76** Average Purchase Amount
- **3.75** Average Review Rating
- % of Customers by Subscription Status (27% Yes, 73% No)
- Revenue & Sales by Category and Age Group
- Filters: Subscription Status, Gender, Category, Shipping Type

---

## 💡 Business Recommendations

- **Boost Subscriptions** – Promote exclusive perks to convert the 73% non-subscribers
- **Customer Loyalty Programs** – Reward returning buyers to push them into the "Loyal" segment
- **Review Discount Policy** – ~50% discount rates on some products risk margin erosion
- **Product Positioning** – Feature top-rated items (Gloves, Sandals) in marketing campaigns
- **Targeted Marketing** – Focus on Young Adults and Express Shipping users for highest ROI

---

## 📁 Project Structure

```
customer-shopping-analysis/
│
├── data/
│   └── shopping_behavior.csv         # Raw dataset
│
├── notebooks/
│   └── eda_cleaning.ipynb            # Python EDA & cleaning notebook
│
├── sql/
│   └── business_queries.sql          # All 10 PostgreSQL queries
│
├── dashboard/
│   └── customer_behavior.pbix        # Power BI dashboard file
│
└── README.md
```

---

## 🚀 How to Run

### Python
```bash
pip install pandas sqlalchemy psycopg2
jupyter notebook notebooks/eda_cleaning.ipynb
```

### PostgreSQL
```bash
psql -U your_user -d your_db -f sql/business_queries.sql
```

### Power BI
Open `dashboard/customer_behavior.pbix` in Power BI Desktop.

---



## 👤 Author

**Harsh Jagdale**
- GitHub: [@Harsh-J17](https://github.com/Harsh-J17)
- LinkedIn: [Harsh Jagdale](https://www.linkedin.com/in/harsh-jagdale-b37635332)
---

## 📄 License

This project is open source under the [MIT License](LICENSE).
