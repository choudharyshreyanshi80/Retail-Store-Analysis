# Retail Store Footfall vs. Sales Analysis

## Project Overview

**Retail Store Footfall vs. Sales Analysis** is an end-to-end data engineering and analytics project that analyzes the relationship between customer footfall and retail sales performance across multiple stores.

The project integrates retail sales and customer footfall data, processes it using Azure data engineering services, and transforms it into meaningful business insights through Power BI dashboards.

It helps businesses understand customer traffic patterns, identify peak shopping hours, evaluate store performance, and analyze how customer visits contribute to sales.

## Objectives

- Analyze the relationship between customer footfall and sales.
- Measure store-wise revenue and transaction performance.
- Calculate customer conversion rates.
- Identify peak shopping hours and high-performing stores.
- Build a scalable data processing workflow using Azure services.
- Present business insights through interactive Power BI dashboards.

## Technologies Used

| Technology | Purpose |
|---|---|
| Azure Data Lake Storage Gen2 | Stores raw and processed datasets |
| Azure Data Factory | Data ingestion and pipeline orchestration |
| Azure Databricks | Data processing and transformation |
| PySpark | Data cleaning, transformation, and aggregation |
| Delta Lake | Stores processed data in Delta format |
| Power BI | Interactive dashboards and data visualization |

## Project Architecture

The project follows the **Medallion Architecture**, organizing data into three layers:

```text
       Source Datasets
              |
              v
   Azure Data Factory
              |
              v
   Azure Data Lake Storage
              |
              v
       Bronze Layer
       (Raw Data)
              |
              v
   Azure Databricks
       (PySpark)
              |
              v
       Silver Layer
   (Cleaned Data)
              |
              v
   Gold Layer
   (Aggregated Data)
              |
              v
          Power BI
     (Interactive Reports)
```

## Medallion Architecture

### 1. Bronze Layer – Raw Data

The Bronze layer stores the original source datasets in their raw format.

**Activities:**
- Ingest raw retail datasets.
- Store source files in Azure Data Lake Storage Gen2.
- Preserve the original data for further processing.

### 2. Silver Layer – Cleaned Data

The Silver layer contains cleaned and validated data processed using Azure Databricks and PySpark.

**Activities:**
- Handle missing values.
- Remove duplicate records.
- Correct data types.
- Standardize data formats.
- Prepare datasets for analysis.

### 3. Gold Layer – Business-Ready Data

The Gold layer contains transformed and aggregated datasets prepared for business analysis.

**Activities:**
- Combine relevant sales and footfall information.
- Calculate business metrics.
- Generate store-wise and time-based summaries.
- Prepare analytical datasets for Power BI.

## Incremental Data Loading

The project incorporates incremental data loading to process newly available records without repeatedly processing the entire dataset.

This approach helps reduce unnecessary processing and improves pipeline efficiency.

## Power BI Dashboards

The project includes two dashboard pages:

### 1. Executive Dashboard

Provides an overview of overall retail business performance.

**Key Performance Indicators (KPIs):**
- Total Revenue
- Total Visitors
- Total Transactions
- Conversion Rate
- Average Rating
- Revenue per Visitor

**Visualizations:**
- Revenue trends
- Store-wise sales performance
- Product category performance
- Footfall vs. sales analysis

### 2. Store Performance & Footfall Analysis

Focuses on store-level performance and customer traffic patterns.

**Visualizations:**
- Hourly footfall analysis
- Hourly sales analysis
- Store-wise conversion rates
- Peak shopping hours
- Revenue by store
- Customer traffic analysis

## Key Business Metrics

| Metric | Description |
|---|---|
| Total Revenue | Total sales revenue generated |
| Total Visitors | Total number of store visitors |
| Total Transactions | Number of completed transactions |
| Conversion Rate | Percentage of visitors who made a purchase |
| Revenue per Visitor | Revenue generated per visitor |
| Average Rating | Average customer rating, where available |

## Project Workflow

1. Collect retail sales and footfall datasets.
2. Ingest source data using Azure Data Factory.
3. Store raw datasets in Azure Data Lake Storage Gen2.
4. Process and clean data using Azure Databricks and PySpark.
5. Organize data into Bronze, Silver, and Gold layers.
6. Apply incremental data loading.
7. Prepare business-ready analytical datasets.
8. Connect the Gold-layer outputs to Power BI.
9. Create interactive dashboards to analyze retail performance.

## Skills Demonstrated

- Data Engineering
- ETL Pipeline Development
- Data Ingestion and Orchestration
- PySpark Data Processing
- Data Cleaning and Transformation
- Delta Lake
- Medallion Architecture
- Incremental Data Loading
- Data Analysis and Visualization
- Power BI Dashboard Development

## Business Benefits

- Helps identify high-performing and low-performing stores.
- Provides insights into customer shopping behavior.
- Helps identify peak customer traffic hours.
- Supports data-driven business decisions.
- Improves understanding of footfall-to-sales conversion.
- Helps businesses evaluate store performance.

## Future Enhancements

- Automate scheduled data refreshes.
- Integrate real-time customer footfall data.
- Introduce predictive sales analytics.
- Develop customer behavior forecasting.
- Add advanced performance monitoring.

---

*This project demonstrates the use of Azure data engineering services and Power BI to transform raw retail data into actionable business insights.*
