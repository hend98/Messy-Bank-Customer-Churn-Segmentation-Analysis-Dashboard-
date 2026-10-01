# Messy Bank — Customer Churn & Segmentation Analysis

## 📊 Project Overview

This project analyzes customer churn for **Messy Bank**, with the goal of understanding where churn is concentrated and identifying customer segments that require further retention analysis.

The analysis goes beyond the overall churn rate by exploring customer behavior across **Geography, Age, Membership Status, Balance, and Number of Products**.

The final Power BI dashboard was designed to answer a key business question:

> **Where is customer churn concentrated, and which customer segments should receive closer retention attention?**

---

## 🎯 Business Objectives

The analysis focuses on four main questions:

* Where is customer churn concentrated geographically?
* Which customer segments show elevated churn rates?
* What customer and account characteristics are associated with churn?
* Which segments combine meaningful customer volume with elevated churn?

---

## 📁 Dataset

The dataset contains **10,000 customer records** with customer-level demographic, geographic, account, and engagement information.

Key fields used in the analysis include:

* Geography
* Age
* Gender
* Credit Score
* Tenure
* Balance
* Number of Products
* Membership Status
* Credit Card Status
* Customer Exit Status

---

## 🛠️ Tools & Technologies

* **Power BI**
* **Power Query**
* **DAX**
* **Data Modeling**
* **Feature Engineering**
* **Data Visualization**
* **Business Analysis**

---

## 🔄 Data Preparation & Feature Engineering

The data was prepared in Power Query and structured for analysis in Power BI.

Key steps included:

* Reviewing the dataset structure and data quality
* Preparing fields for analysis
* Creating customer segments
* Creating a **Balance Segment** feature
* Creating age groups
* Structuring measures for customer counts and churn rates
* Building DAX measures for KPI and segmentation analysis

### Balance Segmentation

Zero-balance customers were **not removed as outliers**.

They represent approximately **36% of the customer base**, making them a substantial customer segment rather than an isolated data point.

Instead, a new categorical feature, **Balance Segment**, was created:

* Zero Balance
* Low Balance
* Medium Balance
* High Balance

This allowed the analysis to compare churn behavior across balance segments without modifying or removing the original customer records.

---

# 📈 Dashboard Pages

## 1. Executive Overview

Provides a high-level view of the customer base and overall churn situation.

### Key KPIs

* Total Customers: **10,000**
* Exited Customers: **2,037**
* Overall Churn Rate: **20.4%**

The page provides the starting point for identifying where churn is concentrated.

---

## 2. Customer & Churn Analysis

This page explores churn across customer characteristics such as:

* Age
* Geography
* Gender
* Credit Score
* Tenure
* Membership Status

The objective is to identify customer groups with noticeably different churn behavior.

---

## 3. Account & Product Analysis

This page focuses on account-level and product-related characteristics, including:

* Balance Segments
* Number of Products
* Membership Status
* Credit Score
* Average Balance
* Credit Card Status

The analysis helps identify relationships between account characteristics and customer churn.

---

## 4. Customer Segmentation & Churn

This page combines **Geography and Age** to identify more specific customer segments.

It focuses on the intersection of:

**Country → Age Group → Customer Volume → Average Balance → Churn Rate**

This allows high-churn segments to be evaluated together with their customer volume rather than looking at churn rate alone.

---

# 🔎 Key Insights

### 1. Overall Churn

The dataset contains **10,000 customers**, with **2,037 exited customers**, resulting in an overall churn rate of **20.4%**.

---

### 2. Germany Has the Highest Country-Level Churn

| Country | Customers | Churn Rate |
| ------- | --------: | ---------: |
| France  |     5,014 |      16.2% |
| Germany |     2,509 |  **32.4%** |
| Spain   |     2,477 |      16.7% |

Germany represents approximately **25% of the customer base**, but accounts for around **40% of all exits**.

This makes Germany an important area for further retention analysis.

---

### 3. Customers Aged 51–60 Show the Highest Overall Churn

| Age Group    | Churn Rate |
| ------------ | ---------: |
| Less Than 30 |       7.6% |
| 30–40        |      11.8% |
| 41–50        |      34.0% |
| 51–60        |  **56.2%** |
| 61+          |      24.8% |

The **51–60** age group has the highest overall churn rate.

---

### 4. Germany — Age 51–60 Is a Key Segment

When Geography and Age are combined, the Germany 51–60 segment stands out:

* **243 customers**
* **10% of Germany's customers**
* **69.5% churn rate**
* Average Balance: approximately **€121.5K**

For comparison, the 51–60 churn rate is:

* France: **52.6%**
* Germany: **69.5%**
* Spain: **46.0%**

This segment combines meaningful customer volume with elevated churn and therefore represents a useful focus area for further retention investigation.

---

### 5. Membership Status Shows a Noticeable Churn Difference

| Membership Status | Churn Rate |
| ----------------- | ---------: |
| Active            |      14.3% |
| Inactive          |  **26.9%** |

Inactive customers show a **12.6 percentage-point higher churn rate** than active customers.

This pattern can be used as an additional area for customer engagement analysis.

---

### 6. Balance Segmentation

| Balance Segment | Churn Rate |
| --------------- | ---------: |
| Zero Balance    |      13.8% |
| Low Balance     |      20.6% |
| Medium Balance  |  **26.4%** |
| High Balance    |      23.0% |

The Zero Balance segment represents approximately **36% of all customers**.

Rather than treating these customers as outliers, they were retained and analyzed as a distinct customer segment.

---

### 7. Number of Products

| Number of Products | Customers | Churn Rate |
| -----------------: | --------: | ---------: |
|                  1 |     5,084 |  **27.7%** |
|                  2 |     4,590 |   **7.6%** |
|                  3 |       266 |      82.7% |
|                  4 |        60 |     100.0% |

Customers with one product represent the largest product segment and have a noticeably higher churn rate than customers with two products.

The very high churn rates among customers with 3 or 4 products were treated cautiously because these groups contain substantially fewer customers.

---

# 💡 Business Takeaway

The analysis shows that customer churn is **not evenly distributed across the customer base**.

The strongest concentration appears in:

> **Germany → Age 51–60 → 69.5% churn**

Rather than applying the same retention approach to every customer, the analysis suggests focusing further investigation on **high-volume, high-churn segments**.

The identified segments can serve as a starting point for deeper analysis of customer behavior, engagement, product usage, and potential retention strategies.

**Important:** These findings describe observed patterns and associations in the dataset. They do not establish that age, geography, membership status, balance, or product count directly causes churn.

---

# 📊 Dashboard Structure

### Page 1 — Executive Overview
High-level customer and churn KPIs.

![Executive Overview](Screenshots/1_Executive%20Overview.png)

### Page 2 — Customer & Churn Analysis
Demographic and customer-level churn patterns.

![Customer Churn Analysis](Screenshots/2_Customer%20Churn%20Analysis.png)

### Page 3 — Account & Product Analysis
Account characteristics, balances, membership, and product usage.

![Account & Product Analysis](Screenshots/3_Account%20&%20Product%20Analysis.png)

### Page 4 — Customer Segmentation & Churn
Detailed segmentation by geography and age to identify high-churn customer groups.

![Customer Segmentation & Churn](Screenshots/4_Customer%20Segmentation%20&%20Churn.png)

---

# 🚀 Project Outcome

The project demonstrates an end-to-end **Data Analyst workflow**:

**Business Problem → Data Preparation → Feature Engineering → Exploratory Analysis → Segmentation → KPI Development → Data Visualization → Business Insights**

The dashboard transforms customer-level data into an interactive analytical tool that helps identify **where churn is concentrated and which segments warrant further investigation**.

---

## 👩‍💻 Skills Demonstrated

**Data Analysis**

* Exploratory Data Analysis
* Customer Segmentation
* Churn Analysis
* Pattern Identification
* Business Insight Generation

**Power BI**

* Interactive Dashboard Design
* DAX Measures
* KPI Development
* Slicers & Filters
* Data Modeling
* Drill-down Analysis

**Power Query**

* Data Preparation
* Transformation
* Feature Engineering

---

## 📌 Project Status

**Completed — Portfolio Project**

Built as an end-to-end customer churn and segmentation analysis project using Power BI.

👩‍💻 Developed By
Hend Abdelnasser (https://www.linkedin.com/in/hend-abd-elnasser-095764218/)

