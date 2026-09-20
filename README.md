# 📊 Online Retail Sales & Customer Behavior Analysis

An exploratory data analysis project on online retail transactions to understand **sales performance, product demand, customer behavior, geographic patterns, time-based trends, and cancellations**.

The project focuses not only on performing analysis, but also on understanding the reasoning behind data cleaning, feature creation, visualization, and business-oriented insights.

---

## 🎯 Project Objectives

* Understand the structure and quality of the retail dataset.
* Clean and prepare transaction data for analysis.
* Analyze overall revenue and product performance.
* Identify high-value and high-frequency customers.
* Compare sales performance across countries.
* Analyze sales patterns across months, weekdays, and hours.
* Investigate cancellations and unusual negative-quantity records.
* Derive business-oriented insights and recommendations.

---

## 🗂️ Dataset

**Dataset:** Online Retail

The dataset contains transactions from a UK-based online retailer between **December 2010 and December 2011**.

### Original Dataset

* **Rows:** 541,909
* **Columns:** 8

### Main Columns

| Column        | Description                      |
| ------------- | -------------------------------- |
| `InvoiceNo`   | Invoice / transaction identifier |
| `StockCode`   | Product identifier               |
| `Description` | Product description              |
| `Quantity`    | Number of units purchased        |
| `InvoiceDate` | Transaction date and time        |
| `UnitPrice`   | Price per unit                   |
| `CustomerID`  | Customer identifier              |
| `Country`     | Customer country                 |

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook
* Git & GitHub

---

## 🔍 Analysis Workflow

```text
Dataset Understanding
        ↓
Data Investigation
        ↓
Data Cleaning
        ↓
Feature Creation
        ↓
Revenue Analysis
        ↓
Product Analysis
        ↓
Customer Analysis
        ↓
Country Analysis
        ↓
Time Analysis
        ↓
Returns & Cancellations
        ↓
Final Insights
        ↓
Business Recommendations
```

---

## 🧹 Data Cleaning

The dataset was investigated before applying cleaning decisions.

Key cleaning steps included:

* Removed duplicate records.
* Investigated missing values.
* Retained missing `CustomerID` records where customer information was not required for the analysis.
* Removed records with missing product descriptions from the main sales dataset.
* Separated negative-quantity records for cancellation/return analysis.
* Excluded transactions with `UnitPrice <= 0` from normal sales analysis.
* Investigated unusually large quantity values instead of automatically removing them.
* Preserved the original dataset for reference.

The resulting normal-sales dataset contained **524,878 records**.

---

## ⚙️ Feature Creation

A new `Revenue` feature was created:

```python
Revenue = Quantity × UnitPrice
```

This feature was used throughout the revenue, product, customer, country, and time analyses.

---

## 📊 Analysis Areas

### 💰 Revenue Analysis

Analyzed:

* Revenue distribution
* Top revenue-generating products
* Quantity vs revenue relationship
* High-value transactions and outliers

### 📦 Product Analysis

Analyzed:

* Products with the highest sales quantity
* Product pricing patterns
* Differences between product demand and revenue contribution
* Non-product transaction types

### 👥 Customer Analysis

Analyzed:

* Unique customers
* Top customers by revenue
* Purchase frequency
* One-time vs repeat customers
* Average and median customer revenue
* Customer revenue distribution
* Customer quantity purchased
* Purchase frequency vs revenue

### 🌍 Country Analysis

Analyzed:

* Sales activity by country
* Revenue by country
* Quantity by country
* Identified customers by country
* Average revenue per customer
* Average revenue per sales record
* Customer count vs revenue

### ⏰ Time Analysis

Analyzed:

* Monthly revenue
* Monthly quantity
* Monthly invoice activity
* Weekday revenue
* Hourly revenue

### 🔄 Returns & Cancellations

Analyzed:

* Negative-quantity records
* Cancellation invoices
* Cancelled quantities
* Cancellation value
* Cancellation rate
* Top cancelled products
* Monthly cancellation patterns
* Unusual large cancellation records

---

## 🧠 Key Findings

* Revenue is highly concentrated among a relatively small number of products and customers.
* Products with the highest quantities sold are not always the products generating the highest revenue.
* Customer revenue is strongly right-skewed, with a smaller group of high-value customers contributing substantially more.
* The **United Kingdom** dominates the dataset in both sales activity and revenue.
* Sales activity increased significantly toward the later months of 2011, with **November** showing particularly high activity.
* Revenue is concentrated mainly during daytime hours.
* Cancellation records represented approximately **1.77% of normal sales records**.
* A few unusually large cancellation records had a substantial effect on total cancelled quantity.
* The dataset contains operational and non-standard records that need to be distinguished from normal product sales.

---

## 📈 Visualizations

The project includes visualizations covering:

* Revenue distribution
* Top products by revenue
* Quantity vs revenue
* Top products by quantity
* Product pricing
* Top customers by revenue
* Customer revenue distribution
* Customer purchasing behavior
* Country revenue and sales patterns
* Time-based sales trends
* Top cancelled products
* Monthly cancellation activity

All major visualizations are saved in the [`images/`](images/) directory.

---

## 💼 Business Recommendations

Detailed recommendations based on the analysis are available in:

**[Business Recommendations](Business_Recommendations.md)**

The recommendations cover:

* High-value products
* High-value customers
* Inventory planning
* High-demand periods
* Geographic markets
* Large cancellation investigation
* Separation of operational records from normal sales analysis

---

## 📁 Project Structure

```text
online-retail-sales-analysis/
│
├── Data/
│   └── Online Retail.xlsx
│
├── notebooks/
│   └── online_retail_eda.ipynb
│
├── images/
|
│── requirements.txt
│   
│
├── Business_Recommendations.md
│
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project

```bash
cd online-retail-sales-analysis
```

### 3. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
                or
pip freeze > requirements.txt

```

### 4. Open the notebook

```bash
jupyter notebook
```

Then open:

```text
notebooks/online_retail_eda.ipynb
```

---

## 📌 Conclusion

This project demonstrates an end-to-end exploratory data analysis workflow, from **understanding and cleaning raw transaction data to feature creation, visualization, insight generation, and business recommendations**.

The analysis highlights how careful investigation and business context are important when working with real-world datasets, especially when dealing with missing values, unusual transactions, cancellations, and outliers.

---

## 🔗 Dataset Source

UCI Machine Learning Repository — Online Retail Dataset

https://archive.ics.uci.edu/dataset/352/online+retail
