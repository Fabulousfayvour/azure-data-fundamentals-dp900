# Provisioning an Azure SQL Database

This document describes the step-by-step process I used to provision an **Azure SQL Database** as part of the Microsoft Azure Data Fundamentals (DP-900) learning path.

---

##  Objective

To create a fully functional Azure SQL Database instance for practicing relational data concepts in Azure.

---

##  Prerequisites

- Active Azure subscription (Free tier or Pay-As-You-Go)
- Azure Portal access (https://portal.azure.com)
- Resource Group (existing or new)

---

##  Step-by-Step Provisioning Process

### 1️⃣ Sign in to Azure Portal
Go to: https://portal.azure.com and sign in with your Microsoft account.

---

### 2️⃣ Create a Resource Group (Optional)
1. Search **Resource groups**
2. Click **Create**
3. Provide:
   - Resource group name: `DP-700-free`
   - Region: (e.g., South Africa North)
4. Click **Review + Create**

---

### 3️⃣ Create Azure SQL Database

1. In the Azure Portal, search **SQL databases**
2. Click **Create**

---

### 4️⃣ Configure Database Basics

Fill in the following details:

- **Subscription:** Your Azure subscription  
- **Resource Group:** `rg-sql-labs`  
- **Database Name:** `dp900-sql-db`  
- **Server:** Create new server  

---

### 5️⃣ Create SQL Server

Click **Create new server** and configure:

- **Server name:** unique-name-sql-server  
- **Location:** Same as resource group  
- **Authentication method:** SQL authentication  
- **Admin login:** sqladmin  
- **Password:** Strong password  

Click **OK**

---

### 6️⃣ Configure Compute + Storage

- Service tier: **Basic** or **General Purpose**
- Compute tier: **DTU-based** (for learning)
- Storage: Default

    - Note: For free learning, Basic tier is recommended.

---

### 7️⃣ Networking Configuration

- Connectivity method: **Public endpoint**
- Allow Azure services and resources to access this server: **Yes**
- Add client IP: **Yes**

---

### 8️⃣ Review and Create

1. Click **Review + Create**
2. Validate configuration
3. Click **Create**

Deployment takes 1–3 minutes.

<img width="899" height="494" alt="deployment-new-sql-database" src="https://github.com/user-attachments/assets/9a99917a-6b96-4f8e-a623-9e77b9cca62c" />

---

## ✅ Verification Steps

1. Go to **SQL databases**
2. Open `dp900-sql-db`
3. Click **Query editor (preview)**
4. Login using SQL admin credentials
5. Run a test query:

```sql
SELECT name FROM SalesLT.Product;
```

<img width="826" height="500" alt="first-azure-sql-query" src="https://github.com/user-attachments/assets/75133975-a17c-48c0-b1fc-217276512a41" />
