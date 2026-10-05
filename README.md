# Power BI Data Modelling Project

A dimensional data modelling project built with **Power BI and Power Query**, transforming multiple operational data sources into a structured analytical model.

## Project Overview

This project involved preparing, transforming, and modelling business data to create an analytical model capable of supporting reporting across sales, customers, products, inventory, campaigns, order processing, and regional performance.

The model is primarily built around a **sales star schema**, with additional related fact tables and specialised modelling structures.

## Data Model

The core sales star schema consists of:

* `fact_sales`
* `dim_customer`
* `dim_product`
* `dim_geo`
* `dim_date`
* `dim_order_flags`

Additional modelling structures were created for:

* Inventory
* Sales targets
* Campaign activity and spend
* Promotion coverage
* Order processing
* Regional access control

## Project Highlights

### Sales Star Schema

The core sales model was structured around a central `fact_sales` table with related dimension tables.

![Sales star schema](images/S10-sales-star-schema-design.png)

### Campaign Modelling

Campaign activity was modelled separately to support campaign performance and promotion analysis.

![Campaign model](images/S16-campaign-model.png)

### Row-Level Security

Row-Level Security was implemented to restrict users to the regional data they are authorised to access.

![RLS customer data](images/S25-rls-customer-data-as-user.png)

## Key Work

* Assessed and cleaned multiple operational source tables.
* Used **Power Query** to transform, merge, append, and standardise data.
* Created reusable dimension and fact tables using reference queries.
* Developed analytical keys including `product_key`, `campaign_key`, `geo_key`, and `flag_key`.
* Built relationships between fact and dimension tables.
* Implemented an **accumulating snapshot** for order-to-payment processing.
* Created a shared date dimension for time-based analysis.
* Developed DAX measures for key business metrics.
* Implemented **Row-Level Security (RLS)** to restrict regional data access.
* Performed data validation and quality checks throughout the modelling process.

## Tools

* **Power BI**
* **Power Query**
* **DAX**
* **Excel**

## Key Outcomes

The final model provides a structured foundation for analysing:

* Sales performance
* Customer activity
* Product performance
* Inventory
* Sales targets
* Campaign performance
* Promotion coverage
* Order processing
* Regional activity

  
## Final Model

![Final data model](images/S26-final-model.png)

## Project Documentation

For the full technical walkthrough, including transformation steps, modelling decisions, relationships, validation, and Row-Level Security:
- [Power BI File](PowerBi/power-bi-data-modelling.pbix)
- [Technical Documentation](technical-documentation.md)



