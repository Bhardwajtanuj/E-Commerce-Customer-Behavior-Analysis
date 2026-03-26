# 🛒 E-Commerce Customer Behavior Analysis

### *From Raw Transactions → Actionable Retention Strategy*

---

## 🌌 Project Overview

In modern e-commerce, **customer retention > acquisition**.

This project performs a **deep behavioral analysis on 350 customers** to answer critical business questions:

* Who are the **high-value customers**?
* What drives **satisfaction vs dissatisfaction**?
* Which users are **about to churn**?
* Do **discounts actually work**?

> 💡 This is not just analysis — it's a **decision-making engine** for pricing, retention, and growth strategy.

---

## 📊 Dataset Description

| Feature                  | Description                       |
| ------------------------ | --------------------------------- |
| Customer ID              | Unique identifier                 |
| Gender                   | Male / Female                     |
| Age                      | Customer age                      |
| City                     | Customer location                 |
| Membership Type          | Bronze / Silver / Gold            |
| Total Spend              | Total purchase amount ($)         |
| Items Purchased          | Number of items bought            |
| Average Rating           | Product rating (3.0–4.9)          |
| Discount Applied         | Boolean                           |
| Days Since Last Purchase | Recency metric                    |
| Satisfaction Level       | Satisfied / Neutral / Unsatisfied |

📌 **Dataset Size:**

* 350 rows × 11 columns
* Clean, structured, minimal missing values (0.6%)

---

## ⚙️ Tech Stack

### 🧠 Data Processing

* **Pandas** → Data manipulation & cleaning
* **NumPy** → Numerical operations

### 📈 Visualization

* **Matplotlib** → Core plotting engine
* **Seaborn** → Statistical visualizations

### 🤖 Machine Learning Utilities

* **Scikit-learn**

  * Label Encoding
  * Feature transformation

### 🛠️ Environment

* Python 3.x
* Jupyter Notebook

---

## 🔄 Project Workflow

### 1. Data Loading & Exploration

* Shape: `350 x 11`
* Checked:

  * Data types
  * Statistical summary
  * Distribution patterns

---

### 2. Data Cleaning

* Missing values handled:

  * `Satisfaction Level → Mode Imputation`
* Outlier detection:

  * IQR method applied
  * ✅ No significant outliers found

---

### 3. Feature Engineering

New features created:

* **Age Group**

  * 26–35 (majority)
  * 36–45

* **Churn Risk**

  * Low (0–20 days)
  * Medium (21–40 days)
  * High (40+ days)

* **Encoded Variables**

  * Gender, City, Membership, Satisfaction

---

## 📊 Exploratory Data Analysis (EDA)

### 👥 Customer Segmentation

#### Gender

* 50/50 split
* Males spend **~40% more**
* Insight: Difference driven by **membership tiers**, not gender itself

---

#### 🎯 Age Groups

| Age Group | Avg Spend |
| --------- | --------- |
| 26–35     | $1025     |
| 36–45     | $482      |

📌 Younger segment dominates:

* Higher spend
* Better ratings
* More engagement

---

#### 🏆 Membership Tiers

| Tier   | Avg Spend | Avg Rating |
| ------ | --------- | ---------- |
| Gold   | $1311     | 4.68       |
| Silver | $748      | 4.05       |
| Bronze | $473      | 3.32       |

🚨 **Key Insight:**
Membership tier is the **strongest predictor** of:

* Revenue
* Satisfaction
* Retention

---

#### 🌍 City Performance

Top vs Bottom:

* 🥇 San Francisco → ~$1460 avg spend
* 🔻 Houston → ~$447 avg spend

📌 Insight:

* City ≠ geography effect
* City = **proxy for membership distribution**

---

### 😊 Satisfaction Analysis

* Only **36% satisfied customers**
* Unsatisfied users:

  * Spend **~50% less**
  * Are inactive **2.5× longer**

🚨 This is a **revenue leakage problem**, not just feedback.

---

### 💸 Discount Effectiveness

| Scenario         | Avg Spend |
| ---------------- | --------- |
| With Discount    | $787      |
| Without Discount | $903      |

📌 Interpretation:

* Discounts attract **low-value customers**
* High-value users **don’t need incentives**

---

## 🔥 Churn Risk Analysis

### Distribution:

* Low: 42%
* Medium: 42%
* High: 16%

### Key Insight:

* High churn users:

  * Low spend
  * Low satisfaction
* Medium churn users:

  * ⚠️ **Most critical segment**
  * Still recoverable

---

### 🚨 Risk Concentration

* **Membership:** Bronze > Silver > Gold
* **Cities:** Chicago & Houston

---

## 🔗 Correlation Insights

| Relationship                     | Correlation |
| -------------------------------- | ----------- |
| Spend ↔ Items                    | 0.97        |
| Rating ↔ Satisfaction            | 0.92        |
| Days Since Last Purchase ↔ Spend | -0.54       |

📌 Interpretation:

* Satisfaction directly drives revenue
* Recency is a strong churn signal

---

## 🎯 Business Insights & Strategy

### 1. High Churn Customers (40+ days)

* Personalized email campaigns
* 15–20% limited-time discount
* Membership upgrade push (Bronze → Silver)

---

### 2. Medium Churn (21–40 days)

* Flash sales (SMS / push)
* Restock notifications
* Loyalty incentives

---

### 3. Low Churn (Active Users)

* Upselling bundles
* Early access for Gold members
* Review generation

---

### 4. Unsatisfied Customers

* Respond within 48 hours
* Short feedback loop
* Recovery incentives

---

### 5. Geographic Strategy

* High-value cities → Membership upgrades
* Low-value cities → Discounts first

---

## 📈 Key Metrics Summary

* 👥 Total Customers: **350**
* 💰 Avg Spend: **$845**
* 😊 Satisfaction Rate: **36%**
* ⚠️ High Churn Risk: **16%**
* 🏆 Top Tier: **Gold**
* 🌍 Top City: **San Francisco**

---

## 🚀 Key Takeaways

1. **Membership tier = revenue engine**
2. Satisfaction is directly tied to **retention & spend**
3. Medium churn users are the **hidden opportunity**
4. Discounts should be **targeted, not global**
5. Customer inactivity = **early churn signal**

---

## 🧠 Future Improvements

* Build a **Churn Prediction Model (ML)**
* Integrate **RFM Analysis**
* Apply **Clustering (K-Means / DBSCAN)**
* Deploy as a **dashboard (Streamlit / Power BI)**
* Real-time recommendation system

---

## 📂 Project Structure

```
📦 ecommerce-analysis
 ┣ 📜 ecommerce_customers.csv
 ┣ 📓 analysis.ipynb
 ┣ 📊 figures/
 ┃ ┣ fig1_gender.png
 ┃ ┣ fig2_age_groups.png
 ┃ ┣ fig3_membership.png
 ┃ ┗ ...
 ┣ 📄 README.md
```

---




