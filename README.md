# Big_Data_Project

ATM Cash Demand Forecasting Pipeline
An end-to-end Big Data pipeline built on Databricks that processes historical RBI cash withdrawal data to forecast future demand using the Prophet model.

Project Overview
This project demonstrates a scalable Medallion Architecture (Bronze/Silver/Gold) for time-series forecasting. We ingested 65 separate data sources, transformed them using Apache Spark, and utilized Prophet to predict cash requirements for the next 90 days, accounting for regional holidays in Tamil Nadu.

Technical Architecture
The project follows the Big Data methodology of separating storage and compute:

Ingestion (Bronze Zone): Raw Excel data (.xlsx) stored in Databricks Unity Catalog Volumes.

Transformation (Silver Zone): A Spark job cleans and standardizes 65 individual sheets into clean CSV files.

Data Warehouse (Gold Zone): Final aggregated and typed data is saved into an Apache Hive managed table (atm_forecast_gold).

Analytics & Visualization: The Prophet model reads from Hive to generate forecasts, components, and a calendar heatmap.

Tech Stack
Platform: Databricks

Engine: Apache Spark (PySpark)

Storage: Unity Catalog Volumes (HDFS Equivalent)

Warehouse: Apache Hive

Forecasting: Meta Prophet

Environment: Jupyter-style Notebooks

Key Results
Trend Analysis: Identified long-term growth patterns and stabilization points in cash demand.

Seasonality: Captured weekly peaks (Mondays) and yearly cycles (March and Oct/Nov peaks).

Holiday Impact: Integrated Tamil Nadu specific holidays to adjust forecast accuracy during regional festivals.

Repository Structure
notebook/: The Databricks notebook exported as .ipynb.

report/: Final project report and PPT presentation.

README.md: Project documentation.
