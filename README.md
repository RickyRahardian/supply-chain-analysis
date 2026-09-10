# Supply Chain Performance & Logistics Dashboard (Power BI)

## Project Overview

This project presents an end-to-end **Supply Chain & Logistics Dashboard** built with **Power BI**. Using a clean dataset containing 100 product SKUs across multiple product lines (*skincare, haircare, cosmetics*), this dashboard provides clear visibility into revenue generation, manufacturing efficiency, carrier logistics, and quality control metrics.

The primary objective is to empower supply chain managers with actionable insights to optimize inventory levels, evaluate shipping performance, control production/transportation costs, and minimize defect rates.

---

## Key Metrics & Dashboard Features

- **Executive Supply Chain Overview**: High-level tracking of Total Revenue ($577.6K+), Total Units Sold (46K+), Average Price, and Overall Stock Availability.
- **Manufacturing & Inventory Analysis**: Breakdown of Stock Levels, Order Quantities, Manufacturing Lead Times, and Production Volumes by Product Type and Location.
- **Logistics & Carrier Performance**: Comparison of Shipping Carriers (*Carrier A, B, C*) and Transportation Modes (*Road, Air, Rail, Sea*) across Shipping Times, Costs, and Routes.
- **Quality Control & Risk Management**: Monitoring Defect Rates (Avg ~2.28%) and Supplier Inspection Results (*Pending, Pass, Fail*) to safeguard product quality and supplier dependability.

---

## Data Source & Architecture

The dataset (`supply_chain_data.csv`) is pre-cleaned and structured, featuring 24 key operational metrics including:
- **Product Details**: SKU, Product Type, Price, Availability, Stock Levels, Order Quantities.
- **Financial Metrics**: Revenue Generated, Manufacturing Costs, Shipping Costs, Total Transportation Costs.
- **Operational Lead Times**: Lead Times, Shipping Times, Manufacturing Lead Times.
- **Supplier & Logistics Data**: Supplier Name, Location, Shipping Carriers, Transportation Modes, Routes, Inspection Results, Defect Rates.

---

## Dashboard Preview

![Supply Chain Dashboard Preview](dashboard_preview.png)

---

## Tools & Technologies Used

- **Power BI Desktop**: Data Modeling, Interactive Visualizations, and Custom DAX Measures.
- **Excel / CSV**: Cleaned Input Data Source (`supply_chain_data.csv`).

---

## DAX Measures Implemented

Key DAX calculations used in the report include:

```dax
// Total Revenue
Total Revenue = SUM(supply_chain_data[Revenue generated])

// Total Products Sold
Total Products Sold = SUM(supply_chain_data[Number of products sold])

// Average Defect Rate
Avg Defect Rate = AVERAGE(supply_chain_data[Defect rates])

// Total Manufacturing Cost
Total Manufacturing Cost = SUM(supply_chain_data[Manufacturing costs])