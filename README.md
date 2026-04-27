# 🚀 End-to-End Azure Data Engineering Pipeline

---

## 📌 Project Overview

This project demonstrates a **production-grade end-to-end data engineering pipeline** built using Azure cloud and PySpark.

The pipeline ingests data from **GitHub REST APIs**, processes it using **Azure Databricks**, and stores it in **Azure Data Lake Gen2** following the **Medallion Architecture (Bronze → Silver → Gold)**.

It simulates how real companies collect, clean, and transform external API data into **analytics-ready datasets**.

---

## 🎯 Business Problem

Organizations need to:
- Track developer activity  
- Monitor repository trends  
- Analyze user engagement  

However, GitHub API data is:
- Semi-structured (JSON)
- Nested and inconsistent
- Not directly usable for analytics  

👉 This pipeline converts raw API data into **clean, structured, and business-ready insights**.

---

## 🏗️ Architecture Diagram

<img width="850" height="350" alt="image" src="https://github.com/user-attachments/assets/e51aeae0-b607-49a1-bdb2-7cc6b91f3896" />



---

## 🧰 Tech Stack

| Technology | Purpose |
|------------|--------|
| Azure Data Factory | Data ingestion & orchestration |
| Azure Data Lake Gen2 | Storage (Bronze, Silver, Gold) |
| Azure Databricks | Data processing |
| PySpark | Data transformation |
| GitHub API | Data source |
| Power BI | Data visualization and reporting |

---
---

## 🔄 End-to-End Workflow

### 1️⃣ Data Ingestion (Bronze Layer)

- Data is extracted from **GitHub REST API**
- Azure Data Factory is used to:
  - Call API endpoints  
  - Fetch JSON data  
  - Store raw data in ADLS  

📌 Output: Raw, unprocessed data

---

### 2️⃣ Data Transformation (Silver Layer)

Performed using **Azure Databricks (PySpark)**:

- Schema enforcement  
- Null value handling  
- Removing duplicates  
- Flattening nested JSON  
- Data type conversion  

📌 Output: Clean, structured dataset

---

### 3️⃣ Data Aggregation (Gold Layer)

- Business logic applied  
- Data aggregated into KPIs  
- Optimized for analytics  

📌 Example:
- User activity metrics  
- Repository engagement  
- Event-based insights  

---

## ⚙️ Pipeline Orchestration

Azure Data Factory controls the workflow:


