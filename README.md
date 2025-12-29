# 🏠 Simplifying Student Housing Through Data & Insights  
**Microsoft Fabric End-to-End Analytics Prototype**

## 📌 Project Overview
This project was developed by members of the **Association for Information Systems (AIS), California State University Long Beach (CSULB)** with the goal of **simplifying student housing decisions using data and insights**.

Over **4 months**, nearly **20 students** collaborated across multiple teams to design and implement a **fully automated, end-to-end data platform** using **Microsoft Fabric**. The final solution was presented at the **Microsoft Fabric User Group**.

I served as the **Lead for the Data Engineering Team**, overseeing architecture design, ingestion strategy, and pipeline implementation.

---

## 👥 Team Structure
- **Business Team** – Requirements gathering, problem definition, and stakeholder alignment  
- **Data Engineering Team** – Data ingestion, ETL pipeline, storage layers, automation *(Lead role)*  
- **Data Analytics Team** – Data modeling, reporting, and visualization  
- **Data Science Team** – Advanced analytics and insight generation  

---

## 🏗️ Architecture Overview
The solution follows a **Medallion Architecture** pattern implemented entirely in **Microsoft Fabric**:

- **Raw** – Source-aligned ingestion  
- **Bronze** – Structured and validated data  
- **Silver** – Cleaned, normalized, analytics-ready data  
- **Gold** – Curated datasets for reporting and insights  

### High-Level Data Flow
![Architecture Diagram](https://github.com/sk7-dev/Student_Housing_Project_AIS-x-Microsoft/blob/main/Images/Dataflow.jpg)

---

## 🔄 ETL Process Breakdown
The ETL pipeline is **fully automated** and processes data incrementally from API sources through multiple transformation layers.

### 🔹 Source → Raw
- Incremental API extraction using **offset-based pagination**
- Pipeline run metadata logged to a **control table**
- Raw data stored with minimal transformation for traceability

### 🔹 Raw → Bronze
- Batch ingestion into structured tables  
- Defined schema for consistent ingestion  
- Parsing of nested JSON into structured columns  
- Tracking table to maintain ingestion run metadata  

### 🔹 Bronze → Silver
- De-duplication of records  
- Column normalization and formatting  
- Quarantine of invalid or error records  
- Tracking table for transformation run metadata  

---

## ⚙️ Implemented ETL Pipeline (Microsoft Fabric)
The ETL workflow is orchestrated using **Microsoft Fabric Pipelines**, with each step executed via notebooks.

![ETL Pipeline Run](https://github.com/sk7-dev/Student_Housing_Project_AIS-x-Microsoft/blob/main/Images/etl_pipeline.png)

### Pipeline Activities
1. **rentcast_api_ingestion** – Incremental API data ingestion  
2. **raw_to_bronze** – Schema enforcement and JSON parsing  
3. **bronze_to_silver** – Data cleansing, normalization, and validation  

---

## 📊 Data Consumers
The curated **Silver and Gold layers** support multiple downstream use cases:
- 📈 **Data Visualization** – Dashboards and reporting  
- 🔍 **Data Analysts** – Ad-hoc analysis and trend discovery  
- 🤖 **Data Scientists** – Feature-ready datasets for modeling  

---

## 🛠️ Technologies Used
- **Microsoft Fabric**
  - Lakehouse
  - Pipelines
  - Notebooks
- **REST APIs** (incremental ingestion)
- **Medallion Architecture**
- **Python / Spark**
- **JSON Processing**
- **Metadata & Control Tables**

---

## 🎤 Presentation & Recognition
- Presented at the **Microsoft Fabric User Group**
- Served as a **real-world, end-to-end analytics prototype**
- Demonstrated cross-functional collaboration and modern data engineering best practices

---

## 🙌 Acknowledgements
Special thanks to:
- AIS CSULB leadership  
- Microsoft Fabric User Group  
- All student contributors across business, engineering, analytics, and data science teams  

---

## 👤 Author
**Shiv Karthee Janardhanan**  
*Data Engineering Lead*  
Association for Information Systems – CSULB
