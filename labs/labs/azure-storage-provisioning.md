# Provisioning an Azure Storage Account

This document outlines the step-by-step process used to provision an **Azure Storage Account** and configure its core services, including:

- Blob Storage  
- Azure Data Lake Storage Gen2  
- Azure Files  
- Azure Tables  

This lab was completed as part of the Microsoft Azure Data Fundamentals (DP-900) learning path.

---

##  Objective

To create a general-purpose Azure Storage Account and explore different storage services for structured and unstructured data workloads.

---

##  Prerequisites

- Active Azure subscription  
- Azure Portal access (https://portal.azure.com)  
- Resource Group (existing or new)  

---

## 🚀 Step-by-Step Provisioning Process

---

## 1️⃣ Create a Resource Group (Optional)

Create a new resources or use an existing resources

---

## 2️⃣ Create Azure Storage Account

1. Search **Storage accounts**
2. Click **Create**

### 🔹 Basic Configuration

- Subscription: Your subscription  
- Resource Group: `DP-700-free`  
- Storage account name: `msstorage11` (must be globally unique)  
- Region: Same as resource group  
- Performance: **Standard**  
- Redundancy: **LRS** (for learning and cost efficiency)  

Click **Review + Create** → **Create**
<img width="908" height="485" alt="Azure-storage-deployment-creation" src="https://github.com/user-attachments/assets/61e1a171-f679-40c4-80cc-ca30f03b6ef0" />

---

#  Storage Services Configuration

---

## 3️⃣ Blob Storage (Unstructured Data)

### 🔹 Purpose  
Used for storing unstructured data such as images, videos, logs, and documents.

### 🔹 Steps

1. Open the storage account  
2. Go to **Containers** under Data Storage  
3. Click **+ Container**
4. Enter:
   - Name: `raw-data`
   - Public access level: Private  

---

## 4️⃣ Azure Data Lake Storage Gen2 (Hierarchical Namespace)

### 🔹 Purpose  
Optimized for big data analytics with hierarchical file system support.

### 🔹 Steps

1. During storage account creation, enable:
   - ✅ **Hierarchical Namespace**
2. After creation, go to **Containers**
3. Create a container:
   - Name: `datalake`
- Load datasets into Blob and Data Lake for analytics  

---

### ⚠️ Note on ADLS Gen2 Upgrade

Some storage accounts cannot be upgraded to ADLS Gen2 after creation due to configuration limitations.  
The recommended approach is to enable **Hierarchical Namespace during storage account creation**.

---

## 5️⃣ Azure Files (File Shares)

### 🔹 Purpose  
Provides cloud-based file shares accessible via SMB or NFS.

### 🔹 Steps

1. In the storage account, go to **File shares**
2. Click **+ File share**
3. Enter:
   - Name: `sharedfiles`
   - Tier: Transaction optimized  

---

## 6️⃣ Azure Tables (NoSQL Key-Value Storage)

### 🔹 Purpose  
Used for storing structured NoSQL key-value data.

### 🔹 Steps

1. Go to **Tables**
2. Click **+ Table**
3. Enter:
   - Table name: `yourtablename`

---

# ✅ Verification Steps

- Upload a sample file to Blob Storage  
- Create directories in Data Lake container  
- Map Azure File Share locally using SMB  
- Insert test entities into Azure Table Storage  

---

## 📌 Learning Outcomes

Through this lab, I gained practical understanding of:

- Azure Storage architecture and services  
- Differences between Blob Storage, ADLS Gen2, Files, and Tables  
- Cloud storage redundancy and performance tiers  
- Real-world storage provisioning and configuration  


---

**Part of my Cloud Data Engineering learning journey (DP-900 → DP-700).**
