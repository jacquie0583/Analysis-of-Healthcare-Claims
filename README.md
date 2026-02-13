# Real-Time Patient Flow Analytics on Azure
Multifacted project focusing on created to transform scripts into standardize format to allow for easy ingestion to fit the expected output,thus allowing any data product would simply ingest the new data without any issues. 
<p align="center">
   <img width="800" height="400" src="https://github.com/jacquie0583/Analysis-of-Healthcare-Claims/blob/main/Picture1.png">   
</p> 

#  Pipeline

<p align="center">
   <img width="800" height="400" src="https://github.com/jacquie0583/Analysis-of-Healthcare-Claims/blob/main/481622958-cb1a1775-ab64-45d7-b45b-50ba97660e1d.png">   </p> 
   
# 🎯 Objectives

      Collect real-time patient data via Azure Event Hub.
      
      Process and cleanse data using Databricks (Bronze → Silver → Gold layers).
      
      Implement a star schema in Synapse SQL Pool for efficient querying.
      
      Enable Version Control with Git.

#  🛠️ Tools & Technologies

   Azure Event Hub – Real-time data ingestion
   Azure Databricks – PySpark-based ETL processing
   Azure Data Lake Storage – Staging raw and curated data
   Azure Synapse SQL Pool – Data warehouse for analytics
   Power BI – Dashboarding (future step)
   Python 3.13+ – Core programming
   Git – Version control

#  📐 Data Architecture
   The pipeline follows a multi-layered architecture:

   Bronze Layer: Raw JSON data from Event Hub stored in ADLS.
   Silver Layer: Cleaned and structured data (validated types, null handling).
   Gold Layer: Aggregated and transformed data ready for BI consumption.

#  ⚙️ Step-by-Step Implementation
      1. Event Hub Setup
      Created Event Hub namespace and patient-flow hub.
      Configured consumer groups for Databricks streaming.
      
      2. Data Simulation
      Developed Python script patient_flow_generator.py to stream fake patient data (departments, wait time, discharge status) to Event Hub.
      Producer Code
      
      3. Storage Setup
      Configured Azure Data Lake Storage (ADLS Gen2).
      Created containers for bronze, silver, and gold layers.
      
      4. Databricks Processing
      Notebook 1: Reads Event Hub stream into Bronze.
      Notebook 2: Cleans and validates schema.
      Notebook 3 : Aggregates and prepares star schema tables.
      
      5. Synapse SQL Pool
      Created dedicated SQL Pool.
      Executed schema and fact/dimension creation queries from:
      DDL_Qureis
      
      6. Version Control
      Version control with Git:
      Commands reference
#  📊 Data Analytics

      Once the data pipeline was established and a Star Schema implemented in Synapse SQL Pool, the next step was to build an interactive dashboard in Power BI.

## 🔗 Synapse → Power BI Connection
      Connected Azure Synapse SQL Pool to Power BI using a direct SQL connection.
      Imported FactPatientFlow and Dimension tables.
      Established relationships for Star Schema-based reporting.

##  📈 Dashboard Features
   The Healthcare Patient Flow Dashboard provides insights into:
   
      Bed Occupancy Rate by department and gender.
      Patient Flow Trends (admissions, wait times).
      Department-Level KPIs (length of stay, Total Patients).
      Interactive Filters & Slicers for gender.

<img width="1228" height="702" alt="image" src="https://github.com/user-attachments/assets/0fb37aaf-5c87-48df-9aa7-0b0a19a748f5" />


#  ✅ Key Outcomes

      End-to-End Pipeline: From real-time ingestion → transformation → warehouse → analytics.
      
      Scalable Architecture: Easily adaptable for different hospital datasets.
      
      Business Insights: Hospital admins can monitor bed usage, patient flow, and department efficiency in real time.
      
      Portfolio Value: Demonstrates both Data Engineering and Analytics skills in one project.
