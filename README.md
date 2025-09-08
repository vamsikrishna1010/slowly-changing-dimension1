# SCD Type 1 SQL Procedures

This repository contains SQL stored procedures for implementing **Slowly Changing Dimension Type 1 (SCD1)** logic in a data warehouse.

## 📄 Files

- `scd1_customer.txt`: Handles customer data updates
- `scd1.txt`: Handles employee data updates

## 🧠 What is SCD Type 1?

SCD1 is a method for managing dimension data where **changes overwrite existing records**. No historical data is preserved.

## 🛠️ Procedure Logic

1. **Create staging and dimension tables** if they don't exist
2. **Insert new records** from staging to dimension
3. **Update existing records** if any field has changed

## 🧪 How to Use

1. Load new data into `*_stg` tables
2. Execute the stored procedure (`EXEC sp_employee` or `EXEC customer`)
3. Query `*_dim` tables to view updated data

## 📬 Contact

For questions or improvements, feel free to open an issue or submit a pull request.
