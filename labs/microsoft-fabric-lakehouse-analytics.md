# Data Analytics in Microsoft Fabric (Lakehouse)

This document describes the step-by-step process of performing data analytics in **Microsoft Fabric**, including creating a workspace, creating a lakehouse, ingesting data, querying data, and cleaning up resources.

This lab was completed as part of the Microsoft Azure Data Fundamentals (DP-900) learning path and prepares for the DP-700 Fabric Data Engineer Associate track.

---

## Objective

To explore Microsoft Fabric analytics capabilities using a Lakehouse architecture for data ingestion and querying.

---

## Prerequisites

- Microsoft Fabric enabled tenant  
- Azure subscription or Microsoft Fabric trial  
- Access to Microsoft Fabric Portal (https://app.fabric.microsoft.com)  

---

## Step-by-Step Process

---

## 1️⃣ Create a Workspace

### 🔹 Steps

1. Go to **Microsoft Fabric Portal**
2. Click **Workspaces**
3. Click **+ New workspace**
4. Provide:
   - Name: `dp900-fabric-workspace`
   - Description: Data engineering learning workspace
   - License mode: Trial or Fabric capacity  

Click **Apply**

---

## 2️⃣ Create a Lakehouse

### 🔹 Steps

1. Inside the workspace, click **+ New**
2. Select **Lakehouse**
3. Enter:
   - Name: `dp900-lakehouse`
4. Click **Create**

---

## 3️⃣ Ingest Data into the Lakehouse

### 🔹 Option A: Upload File (CSV/Parquet)

1. Open the Lakehouse
2. Go to **Files**
3. Click **Upload → Local file**
4. Upload a sample dataset (e.g., sales.csv)

---

### 🔹 Option B: Create a Table from Uploaded Data

1. Navigate to **Tables**
2. Click **New table**
3. Select the uploaded file
4. Choose **Auto-create schema**
5. Click **Load**

---

<img width="908" height="472" alt="image" src="https://github.com/user-attachments/assets/547d84d9-1a9d-49b2-a9bd-797768af1315" />

## 4️⃣ Query Data in the Lakehouse

### 🔹 SQL Query Example

Open **SQL endpoint** or **Notebook** and run:


```sql
SELECT * FROM dp900_lakehouse.sales LIMIT 10;
```

**Aggregation Example**
```SELECT category, SUM(sales_amount) AS total_sales
FROM dp900_lakehouse.sales
GROUP BY category;
```

## 5️⃣ Clean Up Resources

**To avoid unnecessary costs:**


🔹 Delete Lakehouse
- Go to Workspace
- Select Lakehouse
- Click Settings - Delete

🔹 Delete Workspace
- Go to Workspaces
- Select dp900-fabric-workspace
- Click Workspace settings → Delete workspace

### ✅ Verification Steps
- Workspace created successfully
- Lakehouse created and accessible
- Data uploaded and stored in OneLake
- SQL queries executed successfully
- Resources deleted after completion

### 📌 Learning Outcomes
- This lab provided hands-on experience with:
- Microsoft Fabric architecture and OneLake
- Lakehouse vs Data Warehouse concepts
- Data ingestion workflows
- Querying data using SQL in Fabric
- Resource management and cost control
