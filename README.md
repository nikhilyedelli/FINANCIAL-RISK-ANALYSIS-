# Customer Financial Behavior & Risk Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458.svg)
![SciPy](https://img.shields.io/badge/SciPy-Hypothesis%20Testing-8CAAE6.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

# Financial Risk Analysis with Python

## Customer Financial Behavior & Risk Analysis

A data analysis project focused on understanding **customer financial behavior, transaction patterns, account performance, and potential financial risk** using Python.

The project demonstrates an end-to-end financial data analysis workflow, including **data cleaning, transaction analysis, customer profiling, risk identification, exploratory data analysis (EDA), visualization, and statistical hypothesis testing**.

---

## 📌 Project Overview

Financial institutions handle large volumes of customer transaction data. Analyzing this data can help identify:

* Customer transaction behavior
* Credit and debit trends
* High-performing and low-performing accounts
* Customer activity levels
* Dormant accounts
* Negative and near-zero balance accounts
* Large withdrawal patterns
* Potential overdraft situations
* Transaction and balance anomalies
* Potentially suspicious financial activity

This project analyzes transactional customer account data and converts raw financial data into meaningful business insights that can support **customer engagement, account monitoring, and data-driven decision-making**.

---

## 🎯 Project Objective

The main objective of this project is to build a complete **Customer Financial Behavior and Risk Analysis** using Python.

The analysis focuses on answering questions such as:

* How do customers interact with different account types?
* What are the trends in debit and credit transactions?
* Which accounts show unusually high or inconsistent financial activity?
* What transaction behaviors are associated with lower account balances?
* Which accounts may require additional financial monitoring?
* Are differences between customer groups statistically significant?

---

## 🗂️ Project Workflow

```text
Raw Financial Data
        ↓
Data Cleaning & Formatting
        ↓
Descriptive Transaction Analysis
        ↓
Customer Profile Building
        ↓
Financial Risk Identification
        ↓
Exploratory Data Analysis
        ↓
Statistical Hypothesis Testing
        ↓
Business Insights
```

---

# 🛠️ Technologies & Tools

The project uses the following Python libraries and tools:

| Tool / Library   | Purpose                           |
| ---------------- | --------------------------------- |
| Python           | Core programming language         |
| Pandas           | Data manipulation and analysis    |
| NumPy            | Numerical calculations            |
| Regex            | Data cleaning and text processing |
| Matplotlib       | Data visualization                |
| Seaborn          | Statistical visualization         |
| SciPy            | Statistical hypothesis testing    |
| Jupyter Notebook | Analysis and experimentation      |

The report specifically documents the use of **Pandas, NumPy, Regular Expressions, Matplotlib/Seaborn, and SciPy**.

---

# 📊 Dataset

The project uses **financial transactional customer account data**.

The dataset contains information related to:

* Account numbers
* Transaction dates
* Transaction types
* Transaction amounts
* Account types
* Available account balances

Transaction types include:

* Credit
* Debit

The dataset is used to analyze customer financial behavior and identify potential risk indicators.

---

# 🔎 Project Tasks

## Task 1 — Data Cleaning & Formatting

### Objective

Improve the quality and consistency of the raw financial dataset before performing analysis.

### Activities Performed

* Imported required Python libraries
* Loaded the dataset into a Pandas DataFrame
* Inspected data types
* Reviewed descriptive statistics
* Removed special characters from financial columns
* Converted financial fields into numeric format
* Validated transaction dates
* Converted dates into standard `YYYY-MM-DD` format
* Checked Account Type consistency
* Checked Transaction Type consistency
* Saved the cleaned dataset for further analysis

### Result

The cleaning process produced a more consistent and reliable dataset suitable for downstream analysis.

---

# 📈 Task 2 — Descriptive Transaction Analysis

### Objective

Analyze transaction patterns over time and understand customer account behavior.

### Analysis Performed

* Created Year and Month columns
* Calculated monthly credit transactions
* Calculated monthly debit transactions
* Calculated monthly net transaction volume
* Created Credit vs. Debit trend visualizations
* Calculated net inflow for each account
* Identified top-performing accounts
* Identified bottom-performing accounts
* Calculated transaction gaps
* Identified potentially dormant accounts

### Dormant Account Rule

Accounts with a transaction gap of approximately **60 days or more** were flagged as dormant.

### Business Insights

Transaction analysis helps identify:

* Seasonal transaction patterns
* Customer spending behavior
* High and low performing accounts
* Inactive or dormant customers
* Potential opportunities for customer engagement

---

# 👥 Task 3 — Customer Profile Building

### Objective

Categorize customers based on transaction behavior and account balances.

## Activity Level Classification

Customers were classified based on transaction frequency.

| Activity Level  |     Transaction Frequency |
| --------------- | ------------------------: |
| High Activity   |    6 or more transactions |
| Medium Activity |          3–5 transactions |
| Low Activity    | Fewer than 3 transactions |

---

## Customer Segmentation

Customers were segmented using:

* Average Account Balance
* Transaction Volume

The resulting customer segments were:

```text
Premium
Regular
Basic
```

### Customer Profiles

The analysis also identified:

* High Net Inflow Accounts
* High Frequency / Low Balance Accounts
* Negative Balance Accounts
* Near-Zero Balance Accounts

### Business Interpretation

Customers with higher balances and frequent transactions were categorized as Premium customers.

Customers with high transaction frequency but relatively low balances may require closer monitoring.

Negative and near-zero balances were treated as potential financial risk indicators.

---

# ⚠️ Task 4 — Financial Risk Identification

### Objective

Identify accounts that may represent potential financial risk based on transaction behavior.

### Risk Indicators

The project analyzed several financial risk indicators:

### 1. Large Withdrawals

Accounts with withdrawals of:

```text
≥ 75,000
```

were identified.

### 2. Frequent Large Withdrawals

Accounts with **2 or more large withdrawals** were flagged for further analysis.

### 3. Overdraft Accounts

Accounts with a **negative balance** were identified as overdraft accounts.

### 4. Balance Volatility

Balance volatility was analyzed using:

* Standard Deviation
* Coefficient of Variation

### 5. Transaction Anomalies

Potential transaction outliers were identified using:

* IQR — Interquartile Range
* Z-Score

### 6. Suspicious Status

The different risk indicators were combined into a:

```text
SuspiciousStatus
```

column.

Accounts were classified as:

```text
Suspicious
Normal
```

### Business Interpretation

Accounts showing repeated large withdrawals, overdrafts, or abnormal transaction amounts may require additional monitoring.

---

# 📊 Task 5 — Exploratory Data Analysis & Visualization

### Objective

Use visualization to understand customer behavior, transaction patterns, account performance, and financial risk.

### Visualizations Created

The project includes analysis of:

* Transaction Type Distribution
* Account Type Distribution
* Top 10 Net Inflow Accounts
* Bottom 10 Net Inflow Accounts
* Customer Activity Levels
* Customer Segments
* Account Balance Distribution
* Transaction Amount Distribution
* Suspicious vs. Normal Customers
* Correlation Heatmap
* Transaction Amount Outliers
* Balance vs. Transaction Amount
* Dormant vs. Active Accounts

### Charts Used

```text
Bar Charts
Line Charts
Histograms
Boxplots
Scatter Plots
Heatmaps
```

### Business Value

Visualization makes it easier to identify:

* Customer behavior patterns
* Active and inactive accounts
* High-performing accounts
* Potentially suspicious customers
* Transaction anomalies
* Relationships between financial variables

---

# 🧪 Task 6 — Hypothesis Testing

Statistical testing was used to determine whether observed differences between customer groups were statistically significant.

---

## Test 1 — High vs. Low Transaction Volume

Accounts were divided into:

### High-volume accounts

```text
6 or more transactions
```

### Low-volume accounts

```text
2 or fewer transactions
```

An **Independent t-test** was used to compare their average account balances.

The p-value was then used to evaluate the statistical significance of the difference.

---

## Test 2 — Customer Segments

The following customer segments were compared:

```text
Premium
Regular
Basic
```

A **One-Way ANOVA** was used to determine whether average account balances differed between the three groups.

The result was interpreted using the p-value.

---

# 📌 Key Business Insights

The project provides several important analytical insights.

### Customer Behavior

Transaction patterns can help organizations understand customer activity and spending behavior.

### Account Performance

Net inflow can be used to identify high-performing and lower-performing accounts.

### Customer Engagement

Dormant account detection can help identify inactive customers who may require future engagement.

### Customer Segmentation

Customers can be grouped into Premium, Regular, and Basic segments based on account balance and transaction behavior.

### Financial Risk

Negative balances, large withdrawals, repeated large withdrawals, transaction anomalies, and high balance volatility can act as potential risk indicators.

### Data Visualization

Visual analysis helps identify trends, distributions, outliers, and relationships between financial variables.

### Statistical Analysis

Hypothesis testing helps determine whether observed differences between groups may be statistically significant rather than simply caused by random variation.

---

# 📁 Recommended GitHub Repository Structure

```text
financial-risk-analysis-python/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── financial_transactions.csv
│   │
│   └── processed/
│       └── cleaned_financial_transactions.csv
│
├── notebooks/
│   └── Financial_Risk_Analysis.ipynb
│
├── src/
│   ├── data_cleaning.py
│   ├── transaction_analysis.py
│   ├── customer_profiling.py
│   ├── risk_analysis.py
│   ├── visualization.py
│   └── hypothesis_testing.py
│
├── outputs/
│   ├── figures/
│   │   ├── credit_vs_debit.png
│   │   ├── account_distribution.png
│   │   ├── customer_segments.png
│   │   ├── balance_distribution.png
│   │   ├── transaction_distribution.png
│   │   ├── correlation_heatmap.png
│   │   └── suspicious_accounts.png
│   │
│   └── reports/
│       └── Financial_Risk_Analysis_Report.pdf
│
├── requirements.txt
│
└── .gitignore
```

---

# ⚙️ Installation & Setup

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/financial-risk-analysis-python.git
```

Move into the project directory:

```bash
cd financial-risk-analysis-python
```

---

## 2. Create a Virtual Environment

### Windows

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv venv
```

Activate:

```bash
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 📦 Requirements

Create a file named:

```text
requirements.txt
```

Add:

```text
pandas
numpy
matplotlib
seaborn
scipy
jupyter
```

---

# ▶️ Running the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
notebooks/Financial_Risk_Analysis.ipynb
```

Run the notebook cells sequentially.

---

# 🔄 Analysis Pipeline

The complete analysis follows this pipeline:

```text
1. Load Dataset
       ↓
2. Inspect Dataset
       ↓
3. Clean Financial Columns
       ↓
4. Validate Dates
       ↓
5. Standardize Categories
       ↓
6. Analyze Credit & Debit Transactions
       ↓
7. Calculate Net Inflow
       ↓
8. Detect Dormant Accounts
       ↓
9. Build Customer Profiles
       ↓
10. Segment Customers
       ↓
11. Identify Financial Risk
       ↓
12. Detect Outliers
       ↓
13. Perform EDA
       ↓
14. Create Visualizations
       ↓
15. Perform Hypothesis Testing
       ↓
16. Generate Business Insights
```

---

# 📈 Skills Demonstrated

This project demonstrates practical skills relevant to **Data Analyst, Financial Data Analyst, Business Analyst, and Business Analytics** roles.

### Python

* Pandas
* NumPy
* Regular Expressions
* SciPy
* Data manipulation
* Data transformation

### Data Cleaning

* Missing/invalid data inspection
* Data type conversion
* Financial column cleaning
* Date formatting
* Category validation

### Exploratory Data Analysis

* Descriptive statistics
* Distribution analysis
* Correlation analysis
* Outlier detection
* Transaction analysis

### Financial Analysis

* Credit/debit analysis
* Net inflow
* Account balances
* Withdrawal analysis
* Overdraft identification
* Balance volatility

### Customer Analytics

* Customer segmentation
* Activity classification
* Customer profiling
* Dormant account detection

### Risk Analytics

* Large withdrawal detection
* Overdraft detection
* IQR outlier detection
* Z-score analysis
* Suspicious account classification

### Statistics

* Independent t-test
* One-Way ANOVA
* p-value interpretation

### Data Visualization

* Matplotlib
* Seaborn
* Bar charts
* Line charts
* Histograms
* Boxplots
* Scatter plots
* Heatmaps

---

# 💼 Business Use Cases

The analytical approach demonstrated in this project can support several business activities:

### Customer Engagement

Identify dormant or inactive accounts for potential engagement campaigns.

### Risk
