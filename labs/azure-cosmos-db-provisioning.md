# Provisioning Azure Cosmos DB (NoSQL)

This document describes the process of creating an **Azure Cosmos DB account**, setting up a sample database, inserting items, and querying data.  
This lab was completed as part of the Microsoft Azure Data Fundamentals (DP-900) learning path.

---

## Objective

To explore Azure Cosmos DB as a non-relational (NoSQL) database and understand its core components, including accounts, databases, containers, and items.

---

## Prerequisites

- Active Azure subscription  
- Azure Portal access (https://portal.azure.com)  
- Resource Group (existing or new)  

---

# Step-by-Step Process

---

## 1️⃣ Create a Cosmos DB Account

### 🔹 Steps

1. In Azure Portal, search **Azure Cosmos DB**
2. Click **Create**
3. Choose **Azure Cosmos DB for NoSQL**
4. Click **Create**

### 🔹 Configure Basics

- Subscription: Your subscription  
- Resource Group: `yourresourcesgroup`  
- Account Name: `dp900-cosmos-account` (must be globally unique)  
- Location: Africa or US (or preferred region)  
- Capacity mode: **Provisioned throughput** (for learning)  

Click **Review + Create** → **Create**

<img width="454" height="448" alt="Azure-Cosmos-DB-deployment" src="https://github.com/user-attachments/assets/05467e97-ed20-47a6-afa6-62e72b0b1c9b" />


---

## 2️⃣ Create a Sample Database

### 🔹 Steps

1. Open the Cosmos DB account  
2. Go to **Data Explorer**  
3. Click **New Database**
4. Enter:
   - Database ID: `sampledb`
   - Throughput: 400 RU/s (or shared throughput)  

Click **OK**

---

## 3️⃣ Create a Container (Collection)

### 🔹 Steps

1. Inside `sampledb`, click **New Container**
2. Enter:
   - Container ID: `items`
   - Partition key: `/category`
   - Throughput: 400 RU/s (or shared)  

Click **OK**

---

## 4️⃣ View and Create Items

### 🔹 Create Sample Items

1. Open the `items` container  
2. Click **Items → New Item**
3. Insert a sample JSON document:

```json
{
  "id": "1",
  "name": "Laptop",
  "category": "Electronics",
  "price": 1200
}
```

### 🔹 View Items
- Navigate to Items
- Select the document to view its JSON structure

### 🔹Query the Database: Run a SQL Query in Data Explorer
- Click New SQL Query and run:

```SELECT * FROM c```
- Filter Query Example
```SELECT * FROM c WHERE c.category = "Electronics"```

## ✅ Verification Steps
- Confirm Cosmos DB account is active
- Database and container created successfully
- items stored and retrievable
- Queries return expected results

## 📌 Learning Outcomes
**This lab provided hands-on experience with:**

- Azure Cosmos DB architecture (Account → Database → Container → Items)
- NoSQL data modeling and partition keys
- Throughput (RU/s) and scalability concepts
- Querying JSON documents using SQL API
