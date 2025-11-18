# Power-bi-phonepe-project

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
<H1>Loan</H1>

<img width="1050" height="745" alt="Loan" src="https://github.com/user-attachments/assets/fc821dcc-c3e6-4f62-89b7-e19869c2014d" />

<H1>Insurance</H1>

<img width="1329" height="745" alt="Insurance" src="https://github.com/user-attachments/assets/17ab97be-5fe2-409e-8d8c-e6e8276430e6" />

<H1>Money Transfer</H1>

<img width="1045" height="745" alt="Money_Tranfer" src="https://github.com/user-attachments/assets/e0974fc9-393d-4bf3-a5fa-cf0626665cfa" />

<H1>Recharge Bills</H1>

<img width="1048" height="741" alt="Recharge_Bills" src="https://github.com/user-attachments/assets/4d45056e-bd54-46e2-8251-007e64b6e7bb" />

<H1>Conclusion</H1>

This Power BI PhonePe project successfully transforms complex transaction data into a clear, interactive, and actionable dashboard. The primary achievement is the identification of key high-growth segments and regional performance drivers. Moving forward, the focus will shift from descriptive analysis to predictive and prescriptive insights through advanced features like real-time data feeds and forecasting models. This evolution ensures the dashboard remains a strategic asset for data-driven decision-making in expanding PhonePe's market penetration and optimizing product offerings.
