# Task 2: Populating and Cleaning the E-commerce Database

This task focuses on populating the previously designed E-commerce database schema with meaningful sample data, handling missing values thoughtfully, and ensuring the data remains accurate and consistent through appropriate update and delete operations.

## Objective

The goal of this task is to:
- Insert realistic data into each table of the database.
- Manage missing values either by allowing `NULL` or using default values.
- Correct or remove incorrect or incomplete data.
- Maintain referential integrity and follow safe update practices.

##  Database Tables

The schema includes the following six tables:

1. **Customers** – stores information about customers such as name, email, address, and phone.
2. **Categories** – contains product category names.
3. **Products** – stores information about individual products, including name, price, and category.
4. **Orders** – represents customer orders.
5. **Order_Items** – lists individual items within an order.
6. **Payments** – records payment details for each order.

Each table is connected via primary and foreign keys to maintain relational integrity.

## Step 1: Inserting Data

We began by adding meaningful and realistic data into each table. The values chosen represent actual customers, categories, products, orders, and payments.

**Highlights:**
- Each table includes multiple records to reflect real-world variety.
- Data is inserted in the correct order to respect foreign key constraints (e.g., customers before orders, orders before order items).

## Step 2: Handling Missing or Optional Values

In certain cases, not all information was available for specific fields (e.g., a customer’s phone number or product price).

To handle this:
- Optional fields like `Address`, `Phone`, or `Price` were intentionally left empty using a placeholder that indicates missing data.
- For numeric fields such as `Price`, a default value of 0.00 was considered in some cases.
- The database structure was checked to ensure these fields could accept `NULL` values when necessary.

This approach ensures the application can work with incomplete but still valid data without errors.

##  Step 3: Updating Existing Data

After initial data entry, we reviewed the dataset and identified some records that needed correction or completion.

**Examples include:**
- Filling in missing customer addresses or phone numbers.
- Updating a product's price that was initially left blank.

All updates were carefully targeted to specific records to avoid unintended changes to other data.

## Step 4: Deleting Invalid or Test Records

To maintain clean data:
- Certain records that were incomplete or incorrectly inserted (such as products with a price of 0.00) were removed.
- Deletion was done with specific filtering to ensure that only the intended rows were affected.

Since MySQL Workbench may run in Safe Update Mode, deletions were designed to comply with its requirements by including key-based conditions (e.g., using primary keys).

## ✅ Step 5: Data Validation

After performing insert, update, and delete operations:
- Each table was reviewed to ensure data consistency.
- We confirmed that foreign key relationships were intact (e.g., no order pointed to a non-existent customer).
- We verified that no invalid values (like empty mandatory fields or incorrect types) were present.
