# 🚚 Northwind Shipment & Delivery Performance Data Warehouse

## 📌 Purpose

Build a data warehouse using the Northwind database on Azure to analyze shipment and delivery performance.

---

## ⚠️ Business Problem

The Northwind database stores data in normalized operational tables (such as Orders and Shippers), which are not optimized for analytics. This structure makes it difficult to efficiently measure shipping performance or generate insights. Implementing a star schema simplifies analysis and enables effective business intelligence reporting.

---

## 🎯 Objectives

* Design and implement a star schema for shipment/delivery performance
* Load Northwind data into a structured data warehouse
* Develop a BI dashboard to track key shipping performance KPIs

---

## 📦 Scope

### ✔ In Scope

* One business process: **Shipping / Delivery Performance**
* One star schema (one fact table with supporting dimensions)
* Initial data load from Northwind into the data warehouse
* BI dashboard with filtering and drill-down capabilities

### ❌ Out of Scope

* Real-time or streaming data pipelines
* Forecasting or machine learning models
* Additional star schemas beyond project requirements

---

## 📊 Data Sources

The following Northwind tables are used:

* **Orders**

  * Contains order dates (OrderDate, RequiredDate, ShippedDate)
  * Includes shipping details such as ShipVia, ShipCountry, and Freight

* **Shippers**

  * Contains shipper-level information
  * Linked to Orders via ShipVia

---

## 🛠️ Project Plan

1. Review Northwind tables and confirm business requirements
2. Develop a Bus Matrix (Milestone 1)
3. Design star schema (fact + dimension tables)
4. Implement data warehouse tables in Azure
5. Build ETL/ELT pipeline (staging → warehouse) and load data
6. Create BI dashboard and record final demonstration

---

## ⚙️ Functional Requirements

The solution must enable users to:

* Measure shipping duration (e.g., ShippedDate - OrderDate)
* Compare shipping performance across shippers
* Analyze performance over time (day, month, year)
* Evaluate performance by destination (country/region)
* Identify delayed or missing shipments

  * (e.g., ShippedDate is null or exceeds RequiredDate)

Each row in the fact table represents a **shipment event**, making the grain clearly defined for accurate analysis.

---

## 💼 Business Process & Value

### Business Process Modeled

Shipping / Delivery Performance (Orders → Shippers)

### Business Value

This solution enables stakeholders to:

* Monitor shipping efficiency
* Compare carrier performance
* Identify delays and bottlenecks
* Improve operational decision-making and customer satisfaction

---

## 🎯 Mission Statement

Our mission is to build a simple, scalable data warehouse that transforms Northwind operational data into actionable shipment performance insights, supporting data-driven decision-making.

---
