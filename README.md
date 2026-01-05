# Automated-Financial-Market-ETL-Pipeline
## 📖 Project Overview
This project is an end-to-end data pipeline and visualization solution designed to track and analyze the performance of major automotive stocks (Volkswagen, BMW, Mercedes-Benz, Tesla).

The system automates the extraction of raw financial data, transforms it into meaningful technical indicators (Moving Averages, Volatility, Daily Returns), stores it in a relational database, and visualizes it in an interactive Power BI dashboard for trend analysis.


### 🎯 Key Objectives
* **Automate Data Collection:** Remove the need for manual CSV downloads using Python scripts.
* **Technical Analysis:** Calculate key trading metrics like **50-Day Moving Average (MA_50)** and **30-Day Volatility** programmatically.
* **Dynamic Reporting:** Create a "Trader-Style" dashboard with conditional formatting (Red/Green indicators) and interactive time-travel sorting.

## 🏗️ Architecture & Pipeline
**1.Extract**: Python script uses **yfinance** to fetch daily stock data (Open, High, Low, Close, Volume).
pip install yfinance, pandas, sqlalchemy, mysql-connector-python
**jupyter notebook** "Automated Financial Market ETL Pipeline.ipynb"
**2.Transform**: Pandas is used to:
     Clean missing data and handle weekend gaps.
     Calculate Daily Returns %.
     Compute 50-Day Moving Averages (Trend Indicator).
     Compute 30-Day Volatility (Risk Metric).
**3.Load**: Data is pushed into a MySQL database (financial_db) using SQLAlchemy.
**4. Visualize**: Power BI connects directly to MySQL to render the dashboard.

📈 **Future Improvements**
Automated Scheduling: Use Apache Airflow to run the Python script daily.

Cloud Migration: Move the database to AWS RDS and host the dashboard on Power BI Service.

Sentiment Analysis: Integrate news headlines API to correlate stock moves with public sentiment.
