# Customer Financial Behavior & Risk Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458.svg)
![SciPy](https://img.shields.io/badge/SciPy-Hypothesis%20Testing-8CAAE6.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

An end-to-end quantitative financial analytics project prepared for the **Morgan Stanley Executive Leadership Team**. This repository contains data processing pipelines, behavioral profiling, risk flagging algorithms, statistical hypothesis tests, and data visualizations designed to uncover patterns in customer account usage, transaction risk, and financial stability.
Executive SummaryAs digital transactions increase, financial institutions face growing complexity in monitoring account stability and managing risk. This project cleans, transforms, and analyzes transactional data to evaluate how customers interact across account types (e.g., savings, current, credit).Key Deliverables:Behavioral Segmentation: Grouped customers into Premium, Regular, and Basic tiers using balance and activity rubrics.Automated Risk Engine: Rule-based and statistical anomaly detection (IQR, Z-Score) to flag high-risk and suspicious accounts.Statistical Hypothesis Testing: Two-sample t-tests and One-Way ANOVA tests to evaluate statistical differences across transaction volumes and customer segments.Tech Stack & LibrariesLanguage: PythonData Manipulation & Regex: pandas, numpy, reVisualization: matplotlib, seabornStatistical Analysis: scipy.statsProject Architecture & MethodologyThe project is structured into 6 Sequential Tasks:┌─────────────────────────────────────────────────────────────┐
│ 1. Data Cleaning & Formatting                               │
│    • Regex cleaning, numeric parsing, date normalization   │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│ 2. Descriptive Analysis & Dormancy Engine                    │
│    • Net inflow, credit vs. debit trends, 60-day gap flag   │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│ 3. Customer Profiling & Behavioral Segmentation             │
│    • Activity rubrics, segmented tiers, edge-case tracking  │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│ 4. Financial Risk Identification System                     │
│    • Large withdrawals, IQR/Z-score outliers, overdrafts    │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│ 5. Exploratory Data Analysis (EDA)                          │
│    • Volatility heatmaps, distribution plots, scatter plots │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│ 6. Statistical Hypothesis Testing                           │
│    • Independent t-tests & One-Way ANOVA                    │
└─────────────────────────────────────────────────────────────┘
Detailed Task BreakdownTask 1: Data Cleaning & FormattingExtracted and sanitized raw transactional metrics using Regular Expressions (re).Parsed non-numeric characters from currency fields and standardized date columns to YYYY-MM-DD.Verified categorical values across Account Type and Transaction Type.Task 2: Descriptive Transaction AnalysisCalculated monthly transaction volumes, monthly credit/debit aggregates, and net cash inflows.Uncovered top and bottom performing customer accounts.Dormancy Engine: Tracked time gaps between sequential transactions per account; flagged accounts with gaps ≥ 60 days as dormant.Task 3: Customer Profiling & Behavioral SegmentationCustomers were assigned activity levels and business segments according to standard operational rubrics:Activity Rubric:High Activity: ≥ 6 transactionsMedium Activity: 3 - 5 transactionsLow Activity: < 3 transactionsSegment Tiers: Premium, Regular, and Basic based on average balance and activity.Special Risk Profiles: Isolated High Net Inflow, High-Frequency/Low-Balance, Near-Zero Balance, and Negative Balance (Overdraft) accounts.Task 4: Financial Risk IdentificationDeveloped multi-layered risk flags combined into a master Suspicious Status attribute (Suspicious vs. Normal):Large Withdrawal Flags: Single withdrawals ≥ 75,000 or frequent large withdrawals (≥ 2).Overdraft Detection: Identified accounts operating under negative balances.Statistical Anomaly Detection: Applied Interquartile Range (IQR) bounds and Standard Deviation / Z-Score calculations to capture volatile balance patterns and extreme transactional outliers.Task 5: Exploratory Data Analysis (EDA) & VisualizationGenerated a comprehensive visualization suite:Correlation Heatmaps evaluating financial attributes.Distribution charts for Account Types, Transaction Types, and Account Balances.Boxplots highlighting transaction outliers and Scatter Plots mapping Balance vs. Transaction Amounts.Comparative plots contrasting Active vs. Dormant accounts and Suspicious vs. Normal classifications.Task 6: Hypothesis TestingValidated financial assumptions using inferential statistics:Test 1 (Independent t-test): Evaluated if high-volume accounts (≥ 6 transactions) maintain significantly different average balances than low-volume accounts (≤ 2 transactions).Test 2 (One-Way ANOVA): Tested for significant differences in mean balances across Premium, Regular, and Basic customer segments.Dataset StructureThe analysis expects transactional data with the following core schema:FieldTypeDescriptionAccount_NumberString / IntUnique identifier for the customer accountTransaction_DateDate (YYYY-MM-DD)Date of transaction executionTransaction_TypeCategoricalCredit or DebitTransaction_AmountFloatAmount transferred or withdrawnAccount_TypeCategoricalSavings, Current, or CreditAvailable_BalanceFloatRemaining balance after transaction processingQuickstart Guide1. Clone the RepositoryBashgit clone [https://github.com/your-username/financial-risk-analysis-python.git](https://github.com/your-username/financial-risk-analysis-python.git)
cd financial-risk-analysis-python
2. Set Up Virtual Environment & Install DependenciesBashpython -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install pandas numpy scipy matplotlib seaborn
3. Run the PipelineBashpython main.py
Key Business RecommendationsTargeted Re-engagement: Deploy automated outreach campaigns for accounts flagged as dormant (≥ 60 days inactivity) to re-establish relationship momentum.Proactive Risk Monitoring: Monitor accounts flagged as Suspicious due to frequent large withdrawals (≥ 75,000) or balance volatility via automated compliance queues.Tailored Credit Offers: Leverage segment classifications (Premium/Regular/Basic) to customize credit lines and overdraft protection mechanisms.
