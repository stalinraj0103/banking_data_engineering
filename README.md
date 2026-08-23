# 🏦 Banking Data Engineering Project

## 📌 Project Overview

This project demonstrates an end-to-end **Banking Data Engineering pipeline** using **Databricks, PySpark, Apache Spark, and SQL**.

The project starts with raw and messy banking datasets containing customers, accounts, branches, merchants, and transactions. The data is ingested into a **Bronze layer**, cleaned and validated in a **Silver layer**, and transformed into business-ready analytical datasets in a **Gold layer**.

The pipeline follows the **Medallion Architecture**:

```text
Raw Banking Data
       │
       ▼
🥉 Bronze Layer
       │
       ▼
🥈 Silver Layer
       │
       ▼
🥇 Gold Layer
       │
       ▼
Business Analytics


# 🏗️ Data Engineering Architecture

![Banking Data Engineering Architecture](architecture.png)

The project follows the **Medallion Architecture** using Databricks:

```text
                    RAW BANKING DATA
                           │
                           ▼
                 ┌──────────────────┐
                 │  🥉 BRONZE LAYER │
                 │                  │
                 │ Customers        │
                 │ Accounts         │
                 │ Branches         │
                 │ Merchants        │
                 │ Transactions     │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │  🥈 SILVER LAYER │
                 │                  │
                 │ Data Cleaning    │
                 │ Deduplication    │
                 │ NULL Validation  │
                 │ Standardization  │
                 │ Data Validation  │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │   🥇 GOLD LAYER  │
                 │                  │
                 │ Customer KPIs    │
                 │ Branch KPIs      │
                 │ Merchant KPIs    │
                 │ Transaction Data │
                 │ Customer Accounts│
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │ BUSINESS ANALYTICS│
                 │                  │
                 │ Customer Analysis│
                 │ Branch Analysis  │
                 │ Merchant Analysis│
                 │ Transaction KPIs │
                 └──────────────────┘


---

# 📊 KPI Results

Add this section after Architecture:

```markdown
# 📊 Business KPI Results

![Business KPI Results](business_kpis.png)

The Gold layer generates business-ready KPIs from the validated Silver transaction data.

| KPI | Result |
|---|---:|
| 👥 Total Customers | 12,000 |
| 👤 Active Customers | 8,439 |
| 🏦 Total Accounts | 15,000 |
| 🏢 Total Branches | 100 |
| 🛍️ Total Merchants | 2,000 |
| 💳 Total Transactions | 49,980 |
| 💰 Transaction Value | ₹29.98 Crore |
| 💵 Average Transaction Value | ₹5,998.50 |
| ✅ Successful Transactions | 41,432 |
| ❌ Failed Transactions | 2,566 |
| ⏳ Pending Transactions | 3,503 |
| 🔄 Reversed Transactions | 2,479 |
| 📈 Transaction Success Rate | 82.9% |
| 🔁 Duplicate Transaction IDs | 0 |
| 🔗 Unmatched Merchant IDs | 0 |


## 🧮 KPI Calculations

### Transaction Success Rate

Success Rate = Successful Transactions / Total Transactions × 100

= 41,432 / 49,980 × 100

= 82.9%

---

### Average Transaction Value

Average Transaction Value = Total Transaction Value / Total Transactions

= ₹299,805,035.67 / 49,980

= ₹5,998.50

---

### Average Transactions per Customer

= 49,980 / 8,439

= 5.92 transactions/customer

---

### Average Transactions per Branch

= 49,980 / 100

= 499.8 transactions/branch

---

### Average Transactions per Merchant

= 49,980 / 2,000

= 24.98 transactions/merchant


## 🏆 Key Business Insights

- Processed **49,980 validated transactions**.
- Generated approximately **₹29.98 Crore** in transaction value.
- Achieved an **82.9% transaction success rate**.
- Identified **8,439 customers with transaction activity**.
- Average customer processed **5.92 transactions**.
- Each branch processed approximately **499.8 transactions** on average.
- Each merchant processed approximately **24.98 transactions** on average.
- **Healthcare** was the highest transaction category with **6,645 transactions**.
- Detected **0 duplicate transaction IDs** in the final transaction dataset.
- Validated **2,000 merchant IDs** with **0 unmatched merchant IDs**.


┌─────────────────────────────────────────┐
│        BANKING DATA ENGINEERING         │
├─────────────────────────────────────────┤
│ Raw Records              : 79,335       │
│ Silver Records           : 79,080       │
│ Transactions             : 49,980       │
│ Customers                : 12,000       │
│ Active Customers         : 8,439        │
│ Branches                 : 100          │
│ Merchants                : 2,000        │
│ Transaction Value        : ₹29.98 Cr    │
│ Average Transaction      : ₹5,998.50    │
│ Success Rate             : 82.9%        │
│ Gold Tables              : 5            │
│ Duplicate Transactions   : 0            │
│ Unmatched Merchants      : 0            │
└─────────────────────────────────────────┘

This project demonstrates a complete raw-to-analytics banking data pipeline using Databricks and PySpark, following modern Data Engineering practices and the Medallion Architecture.
