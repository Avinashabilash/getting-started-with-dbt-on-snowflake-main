# Tasty Bytes DBT Project

## Project Overview

**Tasty Bytes** is a data transformation and analytics project built using **dbt** on **Snowflake**.  
The project focuses on transforming **Point of Sale (POS) data** from multiple sources into analytics-ready tables for reporting and business insights.  

The goal of the project is to provide clean, reliable, and structured data that can be used for dashboards, business analysis, and performance tracking of food trucks, franchises, locations, menu items, and customer behavior.

---

## Project Objectives

- Standardize raw POS data from multiple source tables.
- Create staging models for initial cleaning and validation.
- Build marts (tables) for analytics and reporting.
- Ensure data quality using dbt tests like `not_null`, `unique`, `relationships`, and value validations.
- Provide an end-to-end workflow from raw data to analytics-ready outputs.

---

## Source Data

The project integrates the following sources:

- **COUNTRY** – Country and city reference data.
- **FRANCHISE** – Information about franchise owners.
- **LOCATION** – Business locations for each food truck.
- **MENU** – Menu items, pricing, and item categories.
- **ORDER_HEADER** – Summary of each order with customer, location, and truck info.
- **ORDER_DETAIL** – Line items for each order, including quantity and price.
- **TRUCK** – Food truck details including franchise association and location.
- **CUSTOMER_LOYALTY** – Customer profile and loyalty information.

---

## Project Workflow

The **Tasty Bytes dbt workflow** follows a structured process from raw data ingestion to analytics-ready tables:

```mermaid
flowchart TD
    A[Raw POS Data in Snowflake] --> B[Staging Models]
    B --> C[Data Cleaning & Validation]
    C --> D[Analytics Marts / Tables]
    D --> E[Business Reporting & Dashboards]
