# SQL Data Warehouse Project

## Overview

This project demonstrates the design and implementation of an end-to-end SQL Data Warehouse using the Medallion Architecture (Bronze, Silver, and Gold layers).

The solution integrates CRM and ERP source systems, applies data quality checks and transformations, and delivers business-ready analytical datasets through a star schema model.

The project showcases practical Data Engineering concepts including ETL development, data modeling, data cleansing, and dimensional design.

---

## Data Architecture

The warehouse follows a Medallion Architecture consisting of three layers:

### Bronze Layer

* Stores raw data from source systems.
* Data is loaded directly from CSV files into SQL Server.
* No business transformations are applied.

### Silver Layer

* Performs data cleansing and standardization.
* Handles duplicate records.
* Fixes invalid dates and data quality issues.
* Standardizes values such as gender, country, and maintenance indicators.
* Cleans hidden source-system characters and formatting issues.

### Gold Layer

* Provides business-ready data models.
* Implements a Star Schema using dimension and fact views.
* Optimized for analytics and reporting.

---

## Project Objectives

* Build a modern SQL Data Warehouse.
* Integrate CRM and ERP data sources.
* Develop ETL processes using SQL Server.
* Implement data quality and validation checks.
* Create dimensional models for reporting and analysis.
* Deliver business-ready datasets for analytics.

---

## Technologies Used

* SQL Server
* T-SQL
* Data Warehousing
* ETL Development
* Dimensional Modeling
* Star Schema Design
* Git & GitHub
* Draw.io

---

## Data Quality Improvements

The Silver Layer implements several data quality rules:

* Removed duplicate customer records using ROW_NUMBER().
* Standardized gender values.
* Standardized country values.
* Corrected invalid sales calculations.
* Corrected invalid and future dates.
* Replaced missing values with appropriate defaults.
* Removed hidden CHAR(13) characters from ERP source data.

---

## Gold Layer Data Model

### Dimension Tables

* dim_customers
* dim_products

### Fact Table

* fact_sales

The Gold Layer follows a Star Schema design to support reporting and analytical workloads.

---

## Repository Structure

scripts/

* bronze/
* silver/
* gold/

datasets/

* CRM source files
* ERP source files

docs/

* Architecture diagrams
* Data models
* Data flow documentation

README.md

---

## Key Skills Demonstrated

* SQL Development
* Data Engineering
* ETL Pipeline Design
* Data Modeling
* Data Cleansing
* Data Warehousing
* Analytical Data Processing
* Star Schema Design
