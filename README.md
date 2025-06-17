# 📊 Banking Risk Analytics Dashboard | Power BI

## 🚀 Project Overview  
This project demonstrates how banks can use **risk analytics** and **data visualization** to reduce financial risk while lending. The interactive Power BI dashboards help assess an applicant’s loan repayment potential based on various client and financial parameters.

## 📁 Dataset Description  
The dataset includes relational tables such as:
- `Clients - Banking`
- `Banking Relationship`
- `Investment Advisor`
- `Gender`
- `Period`

These tables are linked via primary and foreign keys and contain details about client profiles, bank accounts, and financial activities.

## 🛠️ Data Cleaning & Transformation  
- Created **`Engagement Timeframe`** and **`Engagement Days`** columns in the `Clients - Banking` table using DAX `DATEDIFF()`.
- Introduced **Income Bins** using conditional logic to classify estimated income as Low (<100,000) and Mid (<300,000).
- Added **`Processing Fees`** based on the Fee Structure (e.g., 5% for high fees).

## 📐 DAX Calculated Measures  
- `Total Clients` → `DISTINCTCOUNT([Client ID])`
- `Total Loan` → `[Bank Loan] + [Business Lending] + [Credit Card Balance]`
- `Total Deposit` → `[Bank Deposit] + [Savings] + [Foreign Currency] + [Checking]`
- `Total Fees` → `SUMX(Table, [Total Loan] * [Processing Fees])`
- `Engagement Days` → `DATEDIFF(Joined Date, TODAY(), DAY)`

## 📊 KPIs Tracked  
- Total Clients  
- Total Loan, Bank Loan, Business Lending  
- Total Deposits, Fees, Credit Card Balances  
- Savings, Checking & Foreign Currency Account Balances  
- Engagement Length

## 📈 Dashboards & Visuals  
- **Home Dashboard**  
- **Loan Analysis**  
- **Deposit Insights**  
- **Client Summary**  

These dashboards allow banks to:
- Make data-driven loan approval decisions  
- Understand where most deposits originate  
- Analyze credit card usage and engagement timelines  

## ✅ Conclusion  
Using Power BI, this project empowers banking professionals with insights that reduce risk and improve strategic planning. Private banks with higher client counts can be benchmarked, and patterns in loan defaults by nationality or income band can be visualized.

## 🔮 Future Enhancements  
- Analyze client distribution by gender and nationality  
- Predict potential defaulters with machine learning  
- Benchmark banking institutions based on deposit behavior  

---

### 🧠 Tools Used
- Power BI (Data Modeling, DAX, KPI Cards, Slicers, Relationships)
- Relational Data Modeling
- Custom Visuals and Calculated Columns

---

> _Made with ❤️ by Goutham_

