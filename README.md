# Customer_Segmantion_Analysis

## 📌 Project Overview

Customer segmentation is the practice of dividing a customer base into groups based on similarities in demographics or behavior. This project uses K-Means Clustering to segment mall customers based on their Annual Income and Spending Score.
By identifying meaningful groups, businesses can:

---

## 🚀 Objectives

* Perform **Exploratory Data Analysis (EDA)** on customer data
* Segment customers using **K-Means Clustering**
* Visualize different customer segments
* Extract **business insights** from cluster behavior
* Integrate **SQL queries** for data analysis

---

## 📂 Dataset Information

**File:** `Mall_Customers.csv`
**Columns:**

* `CustomerID`
* `Gender`
* `Age`
* `Annual Income (k$)`
* `Spending Score (1-100)`

---

## 🔍 Project Workflow

### 1. Data Loading and Preprocessing

* Loaded dataset using `pandas`
* Handled missing values (none in this dataset)
* Created new derived features (like Spending Category, Age Group)

### 2. Exploratory Data Analysis (EDA)

* Analyzed gender, income, and spending distribution
* Visualized relationships using histograms, pairplots, and heatmaps

### 3. SQL Integration with SQLite

* Connected pandas DataFrame to SQLite
* Ran SQL queries to explore customer patterns (e.g. income vs gender)

### 4. K-Means Clustering

* Used Elbow Method to determine optimal number of clusters
* Applied K-Means to segment customers
* Labeled segments and interpreted cluster behavior

### 5. Data Visualization

* Scatter plots of customer segments
* Cluster coloring based on K-Means labels
* Count plots for gender and age distribution

---

## 📊 SQL Query Examples

```sql
-- Count customers by gender
SELECT Gender, COUNT(*) AS total FROM customers GROUP BY Gender;

-- Average annual income by gender
SELECT Gender, AVG([Annual Income (k$)]) AS avg_income FROM customers GROUP BY Gender;

-- High-income high-spending customers
SELECT * FROM customers WHERE [Annual Income (k$)] > 70 AND [Spending Score (1-100)] > 70;
```

---

## 🧠 Key Insights

* Customers were segmented into **4 distinct groups**
* One cluster included **high-income, high-spending customers** – ideal for premium marketing
* Another cluster had **low-income, low-spending customers** – needs budget offers
* Gender and age trends provide clues for targeted campaigns

---

## 📌 Business Recommendations

* 🎯 Focus premium offerings on Cluster 3 (High income & High spenders)
* 💬 Offer budget bundles to Cluster 1 (Low income & Low spenders)
* 📱 Design targeted ads based on Age Group and Spending Type
* 📈 Use clustering in future recommendation systems

---

## 📎 Folder Structure

```
📁 Customer-Segmentation-KMeans
│
├── Mall_Customers.csv
├── Customer_Segmentation.ipynb
├── README.md
└── requirements.txt (optional)
```
