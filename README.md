# loan-portfolio-dashboard
Interactive Power BI dashboard analyzing 1000 loans — portfolio overview, branch performance &amp; risk analysis
🏦 Loan Portfolio & Risk Analysis Dashboard
![PowerBI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Banking%20%26%20Finance-blue)
> An interactive Power BI dashboard analyzing a loan portfolio of **1,000 loans worth ₹14K** across multiple branches in Maharashtra — covering loan distribution, branch performance, risk assessment, and credit quality.
---
📸 Dashboard Preview
Page 1 — Loan Portfolio Overview
![Loan Portfolio Overview](images/loan_portfolio_overview.png)
Page 2 — Risk & Quality Analysis
![Risk and Quality Analysis](images/risk_quality_analysis.png)
---
📌 Business Problem
A banking institution wants to:
Monitor the health of its loan portfolio across branches
Identify high-risk loan categories and overdue accounts
Understand loan type distribution and revenue contribution
Track NPA (Non-Performing Assets) and default rates over time
---
📊 Dashboard Pages
🔵 Page 1: Loan Portfolio Overview
KPI	Value
Total Loan Amount	14K
Total Loans	1,000
Approved Loans	822
Rejection Rate	0.18
NPA Rate	0.04
Avg Interest Rate	9.46%
Visuals included:
Loan Type Distribution — Donut chart showing Home Loan (41.62%), Personal Loan (23.4%), Auto Loan (13.13%), Business Loan (11.8%), Education Loan (10.05%)
Loan by Branch — Bar chart comparing approved vs. rejected loans across Nagpur, Nashik, Pune, Thane, and Aurangabad branches
Total Loan Amount by Loan Type — Column chart comparing revenue by loan category
Total Loan Amount by Issue Date — Time series chart from Jul 2021 to Jul 2023
Year Slicer — Interactive filter for 2021–2023
---
🔴 Page 2: Risk & Quality Analysis
KPI	Value
Total Defaulted	31
Total Overdue	210
Avg Loan Amount	14.32
Visuals included:
Overdue Bucket Analysis — Bar chart showing loans by overdue days (Current, 1-30, 31-60, 61-90, 90+ days)
Default Rate by Loan Type — NPA rate comparison across Personal, Home, Education, Business, and Auto loans
Credit History Distribution — Donut chart showing 54% vs 46% credit history split
Credit History by Branch — Bar chart showing total overdue across Nagpur, Andheri, Nashik, Kolhapur, Mumbai Central, and Thane
Loan Type Filter — Slicer for Auto, Business, Education loan filtering
---
💡 Key Insights
📍 Home Loans dominate the portfolio
At 41.62% of total loans, Home Loans are the biggest segment — also contributing the highest total loan amount, making them the most critical category to monitor for risk.
📍 Strong approval rate
822 out of 1,000 loans were approved (82.2%), with a rejection rate of just 0.18 — indicating a relatively healthy underwriting process.
📍 Personal and Home Loans have highest default risk
The Risk page reveals that Personal Loans and Home Loans have the highest NPA rates (~0.04), despite being the top two loan categories by volume.
📍 Nagpur branch leads in total loans
Nagpur consistently shows the highest loan volume across branches, while Aurangabad has the lowest — suggesting geographic concentration risk.
📍 Most overdue loans are in the "Current" bucket
The overdue bucket analysis shows the majority of overdue accounts are still in the early stages (Current or 1-30 days), which is a positive sign for recovery.
📍 54% of customers have poor credit history
The credit history donut shows 54% of borrowers fall in the lower credit history category — a risk factor that should be incorporated into future loan approval strategies.
---
🛠️ Tools & Technologies
Power BI Desktop — Dashboard creation and data modeling
DAX — Calculated measures (NPA Rate, Rejection Rate, Avg Interest Rate)
Power Query — Data cleaning and transformation
Data Modeling — Relationships between loan, branch, and customer tables
---
📁 Repository Structure
```
📁 loan-portfolio-dashboard/
│
├── 📄 README.md
├── 📊 Loan_Tracking.pbix          ← Power BI dashboard file
└── 📁 images/
    ├── loan_portfolio_overview.png    ← Page 1 screenshot
    └── risk_quality_analysis.png      ← Page 2 screenshot
```
---
🚀 How to Use
Clone the repo:
```bash
   git clone https://github.com/Akash277-dev/loan-portfolio-dashboard
   ```
Open the `.pbix` file in Power BI Desktop (free download from Microsoft)
Interact with the dashboard using the year slicer and loan type filters
> 💡 If you don't have Power BI Desktop, you can view the dashboard screenshots in the `images/` folder.
---
📈 DAX Measures Used
```dax
-- NPA Rate
NPA Rate = DIVIDE([Total NPA Loans], [Total Loans], 0)

-- Rejection Rate
Rejection Rate = DIVIDE([Total Rejected], [Total Loans], 0)

-- Avg Interest Rate
Avg Interest Rate = AVERAGE(Loans[Interest_Rate])

-- Default Rate by Loan Type
Default Rate = DIVIDE(COUNTROWS(FILTER(Loans, Loans[Status] = "Defaulted")), [Total Loans], 0)
```
---
🧠 Business Recommendations
Monitor Personal and Home Loan defaults closely — These categories have the highest NPA rates despite being the largest segments.
Strengthen credit assessment for high-risk borrowers — With 54% of customers in the lower credit history bracket, tightening eligibility criteria could reduce future NPAs.
Expand in underperforming branches — Aurangabad shows low loan volume, suggesting either low demand or conservative underwriting that could be reviewed.
Early intervention for 1-30 day overdue accounts — Proactive outreach at this stage can prevent accounts from moving into the 90+ day bucket.
---
🙋 About Me
Akash Mishra — Fresher Data Analyst skilled in Python, SQL, and Power BI.
🔗 LinkedIn
🐙 GitHub
---
⭐ If you found this dashboard useful, consider starring the repo!
