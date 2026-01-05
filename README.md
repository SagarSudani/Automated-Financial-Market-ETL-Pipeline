# Automated-Financial-Market-ETL-Pipeline
## 📖 Project Overview
This project is an end-to-end data pipeline and visualization solution designed to track and analyze the performance of major automotive stocks (Volkswagen, BMW, Mercedes-Benz, Tesla).

The system automates the extraction of raw financial data, transforms it into meaningful technical indicators (Moving Averages, Volatility, Daily Returns), stores it in a relational database, and visualizes it in an interactive Power BI dashboard for trend analysis.

Steps
Clone the Repo:

git clone [https://github.com/yourusername/stock-market-etl.git](https://github.com/yourusername/stock-market-etl.git)

### 🎯 Key Objectives
* **Automate Data Collection:** Remove the need for manual CSV downloads using Python scripts.
* **Technical Analysis:** Calculate key trading metrics like **50-Day Moving Average (MA_50)** and **30-Day Volatility** programmatically.
* **Dynamic Reporting:** Create a "Trader-Style" dashboard with conditional formatting (Red/Green indicators) and interactive time-travel sorting.

## 🏗️ Architecture & Pipeline

The project follows a classic **ETL (Extract, Transform, Load)** architecture:
A[Yahoo Finance API] -- Extract --> B(Python Script)
B -- Transform (Pandas) --> C{Clean & Calculate Metrics}
C -- Load --> D[(MySQL Database)]
D -- Connect --> E[Power BI Dashboard]

📈 **Future Improvements**
Automated Scheduling: Use Apache Airflow to run the Python script daily.

Cloud Migration: Move the database to AWS RDS and host the dashboard on Power BI Service.

Sentiment Analysis: Integrate news headlines API to correlate stock moves with public sentiment.
