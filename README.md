# 📦  Load Data into a Warehouse using T-SQL

## 🎯 Purpose of the Lab
This lab demonstrates how to ingest data from a lakehouse into a data warehouse using T-SQL in Microsoft Fabric. It covers the creation of schemas, tables, views, and a stored procedure to load and analyze sales data for large-scale analytics. The goal is to understand how data flows from a data lake to a structured warehouse environment and how SQL-based transformations enable deeper analysis.

---

## 🛠️ Step-by-Step Process 

1. **Create a Fabric Workspace**
   - Logged into Microsoft Fabric and created a new workspace with Fabric trial or premium capacity.

2. **Set Up a Lakehouse and Upload Data**
   - Created a new lakehouse.
   - Downloaded the `sales.csv` file from GitHub.
   - Uploaded the CSV file to the Files folder in the lakehouse.

3. **Create a Table in the Lakehouse**
   - Loaded the uploaded CSV file into a new table named `staging_sales` using Fabric’s built-in table loading feature.

4. **Create a Data Warehouse**
   - Created a new data warehouse in the same workspace.

5. **Create Fact and Dimension Tables**
   - Created the following tables under a new schema named `Sales`:
     - `Fact_Sales`
     - `Dim_Customer`
     - `Dim_Item`
   - Defined primary keys (non-enforced) on the dimension tables.

6. **Create a View**
   - Created a view named `Staging_Sales` in the warehouse that queries the lakehouse `staging_sales` table directly.

7. **Load Data from Staging to Warehouse**
   - Developed and executed a stored procedure `Sales.LoadDataFromStaging` to:
     - Populate `Dim_Customer` and `Dim_Item` with distinct values.
     - Load transactional data into `Fact_Sales`.

8. **Run Analytical Queries**
   - Ran three analytical queries to:
     - Find top customers by total sales.
     - Find best-selling items.
     - Determine the top customer in each category (Bike, Helmet, Gloves).

---

## 📘 What I Learned

- **Workspace & Lakehouse Integration**: Learned how Microsoft Fabric integrates lakehouse and warehouse architectures within the same environment.
  
- **Data Ingestion**: Gained hands-on experience in uploading and preparing CSV files for analysis using lakehouse tables.

- **Warehouse Modeling**: Understood dimensional modeling by creating fact and dimension tables.

- **View & Cross-Database Querying**: Learned how to use views to bridge data between lakehouse and warehouse, enabling cross-storage querying.

- **Stored Procedures**: Practiced writing and executing stored procedures with parameters for dynamic data loading.

- **Analytical Insights**: Developed T-SQL skills by writing aggregate queries to extract insights from warehouse data.

- **Performance Considerations**: Understood the trade-offs of using or skipping foreign key constraints in data warehousing for performance optimization.

This lab provided a comprehensive end-to-end scenario that connects data ingestion, modeling, transformation, and analytics — all using T-SQL in Microsoft Fabric.

---

## 📸 Screenshots

<img width="1438" alt="1" src="https://github.com/user-attachments/assets/b867ef40-6dbd-4dd0-b1e3-2f98e28d7b8f" />

<img width="1384" alt="2" src="https://github.com/user-attachments/assets/10f88f05-12df-4f13-a6ad-a82f308f24c0" />

<img width="1203" alt="3" src="https://github.com/user-attachments/assets/9e29cd5b-132b-4aea-9eb6-d174db4cd30b" />

<img width="1036" alt="4" src="https://github.com/user-attachments/assets/3559fbc6-00be-4018-b2a0-a80d123a9eab" />

<img width="1191" alt="5" src="https://github.com/user-attachments/assets/176a99e8-c4c2-47fa-981d-ef6743a5eaf5" />

<img width="1232" alt="6" src="https://github.com/user-attachments/assets/8ef3deba-fbda-4326-b845-77c1f885e1c4" />

<img width="1428" alt="7" src="https://github.com/user-attachments/assets/ea34cdfd-0fe9-49cc-b5b7-4bba9d213464" />

<img width="1139" alt="8" src="https://github.com/user-attachments/assets/9249a8ad-6e4a-421f-b7a9-2f46fd10681a" />

<img width="1382" alt="10" src="https://github.com/user-attachments/assets/0b6d6d47-6e3c-455d-b29e-1072a19f834a" />

<img width="1414" alt="11" src="https://github.com/user-attachments/assets/88fefeeb-6559-4bfb-85c1-20fc1b3356a5" />
