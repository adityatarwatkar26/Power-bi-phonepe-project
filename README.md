# Power_bi_phonepe_project

![Phonepe_logo](https://img-cdn.publive.online/fit-in/1200x675/entrackr/media/media_files/2025/06/06/5ror6sAJIrteOyjzkoMn.jpg)

<H1>Tool Used :-</H1>

![Power_Bi](https://tse3.mm.bing.net/th/id/OIP.Oxo-u9GMK3zbEM5h-FiVnQHaEK?pid=Api&P=0&h=220)

<H1>Overview</H1>
This project demonstrates a comprehensive analysis of hypothetical PhonePe-like transactional and user data using Microsoft Power BI. The goal is to transform raw, disparate data from various services (Recharge, Money Transfer, Loans, Insurance) into a cohesive and interactive business intelligence dashboard. This dashboard provides key performance indicators (KPIs) and actionable insights into user behavior, service performance, and financial trends.

<H1>Objectives</H1>

- The primary objectives of this Power BI project are to:

- Develop a Robust Data Model: Create a scalable and efficient Star Schema within Power BI to link user demographics with various transaction types.

- Calculate Key Metrics: Use DAX to calculate essential financial and operational KPIs (e.g., Total Transaction Value, Transaction Count, Success Rate, Average Transaction Value, Monthly Active Users).

- Identify Service Performance: Analyze the performance, volume, and growth rates of different PhonePe services (e.g., Money Transfer vs. Loans vs. Insurance).

- Visualize User Behavior: Gain insights into how different user segments (e.g., age groups, joining date cohorts) interact with the application.

- Enable Data-Driven Decisions: Provide an interactive dashboard that allows stakeholders to quickly identify trends, bottlenecks, and areas for strategic focus.

<H1>ETL Process (Extract, Transform, Load)</H1>

The Extract, Transform, and Load (ETL) process is performed primarily within Power Query Editor (M language) in Power BI Desktop to clean, consolidate, and shape the data before it is loaded into the data model.

<H3>1. Extraction</H3>

All seven data sources (All_Users, All_Transactions, and the five service-specific transaction files) are imported into Power Query Editor.

<H3>2. Transformation (Power Query)</H3>

Data Consolidation: The service-specific transaction tables (Recharge_Bills, Money_Transfer, Loans, Insurance) are systematically Appended (union operation) into a single, master transaction fact table. This ensures all transaction data is unified for analysis.

<H3>Data Type Cleaning:</H3>

- Date columns are converted to the proper Date data type.

- Amount columns are converted to Currency or Decimal Number data type.

- Text columns are checked for consistency and trimmed of unnecessary whitespace.

- Standardization: Custom columns are added to the consolidated transaction table to ensure consistent terminology across services (e.g., standardizing 'Service Type' columns).

- Error and Status Handling: The Payment_Status and Reason columns are inspected to identify transaction failure rates, and measures are built to filter for successful vs. failed transactions.

- Date Dimension: A dedicated Date dimension table is generated (or derived from the transaction dates) to support robust time intelligence analysis.

<H3>3. Loading</H3>
   
The transformed and cleaned tables (Users Dimension, Date Dimension, and Master Transactions Fact) are loaded into the Power BI Data Model.

Relationships are established between the tables to create a robust Star Schema (e.g., linking the Master Transactions table to the All_Users table using User_ID, and to the Date table using the Date column).

<H1>📌 Loans</H1>

<H3>🚀 Key Loan Portfolio Highlights</H3>

- Total Portfolio Value: The portfolio holds ₹2.53 billion in loans.
- Success Rate: Payment status is overwhelmingly Successful (accounting for ₹2.43bn), indicating high loan recovery efficiency.
- Volume Stability: The number of loans disbursed monthly is stable (consistently around 4K).
- Value Volatility: Loan amount disbursed shows significant monthly fluctuation, with a peak in July (over ₹220M).
 
<img width="1204" height="741" alt="Loan" src="https://github.com/user-attachments/assets/580f32b9-55a9-458d-b8d4-67a96eee5f0a" />


<H1>📌 Insurance</H1>

<img width="1452" height="741" alt="Insurance" src="https://github.com/user-attachments/assets/5b47bb71-7b4c-4efc-b693-c895b5cb92a4" />


<H1>📌 Money Transfer</H1>

- Total transfer volume and value across UPI transactions.
- User engagement patterns and transfer trends over time.
- Performance comparison of peer-to-peer vs merchant transfers.

<img width="1177" height="754" alt="Money Transfer" src="https://github.com/user-attachments/assets/a68c7b10-9ffc-45d6-a4aa-43b24ebde0d3" />


<H1>📌 Recharge & Bills</H1>

- High-frequency recharge categories and bill payment patterns.
- Peak transaction periods and customer usage trends.
- Success rates and transaction volume comparison across services.

<img width="1109" height="740" alt="Recharge Bills" src="https://github.com/user-attachments/assets/9c4e5735-1572-40de-9bb9-9bbba961002f" />


<H1>Conclusion</H1>

This Power BI PhonePe project successfully transforms complex transaction data into a clear, interactive, and actionable dashboard. The primary achievement is the identification of key high-growth segments and regional performance drivers. Moving forward, the focus will shift from descriptive analysis to predictive and prescriptive insights through advanced features like real-time data feeds and forecasting models. This evolution ensures the dashboard remains a strategic asset for data-driven decision-making in expanding PhonePe's market penetration and optimizing product offerings.
