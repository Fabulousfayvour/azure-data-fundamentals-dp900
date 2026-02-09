# Data Lake Gen2 Upgrade Failure

## ❌ Error Encountered
While working on Azure Storage during the DP-900 learning path, I attempted to upgrade a Storage Account to **Azure Data Lake Storage Gen2** and encountered the following error:

> **HnsOnMigration is not supported for the account**

![WhatsApp Image 2026-02-09 at 01 52 27](https://github.com/user-attachments/assets/9f5db261-8b01-4d00-a7db-403ef027bd84)


---

##  Cause
This error occurs when the storage account configuration does not support enabling Hierarchical Namespace (HNS). Common causes include:

- Storage account type is not StorageV2  
- Unsupported features enabled (blob soft delete, versioning, immutable policies)  
- Subscription or region limitations  
- Legacy storage configurations  

---

## ✅ Resolution
The recommended solution is to create a **new Storage Account with Hierarchical Namespace enabled during creation**, as some accounts cannot be upgraded.

---

## 📌 Learning Outcome
This issue helped me understand:

- Azure Storage account configurations  
- ADLS Gen2 architecture limitations  
- Real-world cloud troubleshooting  
