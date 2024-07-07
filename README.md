# Retail Customer Data Analysis and Database Modeling
#### Subtitle: From Data Cleaning to Relational Database Design
-------------------------------
## Project Overview
This project focuses on cleaning and structuring a retail transaction dataset, followed by designing a relational database to organize the cleaned data effectively. The ultimate goal is to provide a robust data model that supports a detailed analysis of customer behavior and purchasing patterns.

## Business Problem
The dataset contains numerous duplicate values and inconsistencies, such as multiple email addresses or phone numbers for the same customer. These issues complicate the analysis of customer data and hinder the development of accurate customer profiles. To address these challenges, we need to clean the data and create a new, unique identifier for each customer. Additionally, we aim to design a relational database to facilitate efficient data management and querying.

## Steps and Methodology
### 1. Data Cleaning
#### Importing Libraries and Loading Data
- The project begins by importing necessary libraries and loading the dataset.

#### Exploring and Initial Cleaning
- Remove any rows with **null values** in critical columns.
- Remove any duplicated rows.
- Standardize the formatting of columns such as **Email and Phone**.
- Splitting the **name** column to create **First_name** and **Last_name** columns.
#### Converting Datatype
- Converting datatype for **Transaction_ID, Customer_ID, Zipcode, Age, and Total_Purchases.**
#### Handling Dates
- Clean the Date column and create a new **Purchase_Date** column.
#### Investigating IDs
- Investigate **Customer_ID** and **Transaction_ID** to identify inconsistencies.
#### Creating New IDs
- Create new unique identifiers for each **transaction, customer, product, order, and feedback**.
#### Dropping Columns:
- Dropping **Date, Year, Month, Time, Name, Transaction_ID, and Customer_ID**columns.
  
### 2. Creating Individual DataFrames for Each Table
- The cleaned data is split into individual DataFrames for **customers, products, transactions, orders, and feedback.**

### 3. Creating the Relational Database
#### 1. Setting Up the Database and Tables
A **relational database** is set up using **SQLite**, and tables for **customers, products, transactions, orders, and feedback** are created.

#### 2. Inserting Data into Tables
The cleaned and structured DataFrames are inserted into the corresponding tables in the relational database.

## Schema Diagram
![Shema Diagram drawio](https://github.com/SBOSE550/Data-Modeling-Project/assets/98967373/c06d3980-4bbb-4a10-8856-94b3b88a8db8)


## Conclusion
By **cleaning the dataset and designing a relational database**, the project addresses the following issues:

- Eliminates duplicate transaction records, ensuring each transaction is uniquely identifiable.
- Consolidates customer data, even when customers use multiple emails or phone numbers.
- Facilitates efficient querying and analysis by organizing data into related tables.
## Benefits
- **Improved Data Quality**: Removing duplicates and standardizing data formats enhance the accuracy of customer profiles.
- **Efficient Data Management**: A relational database structure supports more efficient data storage and retrieval.
- **Enhanced Analytical Capabilities**: Clean, well-structured data allows for more precise analysis of customer behavior and trends.

## Project Structure
- **data_cleaning_modeling.ipynb:** Jupyter Notebook containing the entire data cleaning and database creation process.
- **retail_data.csv:** The original dataset used in this project.
- **retail_data.db:** The resulting SQLite database file.
- **schema_diagram.png:** The schema diagram illustrating the relational database design.
