# crowdfunding_ETLfin
Project 2: Data Transformation and Database Creation

Libraries to install: To begin the project, make sure you have installed the necessary libraries: Pandas and Numpy. Use the following commands for installation:

- Pandas: conda install pandas
- Numpy: conda install numpy

Instructions:

1. Create the Category and Subcategory DataFrames:
Extract and transform data from the crowdfunding.xlsx Excel file to create a category DataFrame with the following columns:

- "category_id": Sequential entries from "cat1" to "catn," where n is the number of unique categories.
- "category": Contains only the category titles.

Save the category DataFrame as category.csv and store it in your GitHub repository.

Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame with the following columns:

- "subcategory_id": Sequential entries from "subcat1" to "subcatn," where n is the number of unique subcategories.
- "subcategory": Contains only the subcategory titles.

Save the subcategory DataFrame as subcategory.csv and store it in your GitHub repository.

2. Create the Campaign DataFrame:
Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame with the following columns:

- "cf_id"
- "contact_id"
- "company_name"
- "blurb" (renamed to "description")
- "goal" (converted to the float data type)
- "pledged" (converted to the float data type)
- "outcome"
- "backers_count"
- "country"
- "currency"
- "launched_at" (renamed to "launch_date" and with UTC times converted to the datetime format)
- "deadline" (renamed to "end_date" and with UTC times converted to the datetime format)
- "category_id" (with unique identification numbers matching those in the "category_id" column of the category DataFrame)
- "subcategory_id" (with unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame)

Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

3. Create the Contacts DataFrame:

Choose one of the following options to extract and transform data from the contacts.xlsx Excel file:

Option 1: Use Python dictionary methods.
Option 2: Use regular expressions.

If you choose Option 1, follow these steps:

- Import the contacts.xlsx file into a DataFrame.
- Iterate through the DataFrame, converting each row to a dictionary.
- Extract the dictionary values from the keys using a Python list comprehension and add them to a new list.
- Create a new DataFrame containing the extracted data.
- Split each "name" column value into first and last names and place them in separate columns.
- Clean and export the DataFrame as contacts.csv, saving it to your GitHub repository.

If you choose Option 2, follow these steps:

- Import the contacts.xlsx file into a DataFrame.
- Extract the "contact_id," "name," and "email" columns using regular expressions.
- Create a new DataFrame with the extracted data.
- Convert the "contact_id" column to the integer type.
- Split each "name" column value into first and last names and place them in separate columns.
- Clean the DataFrame and export it as contacts.csv, saving it to your GitHub repository.

4. Create the Crowdfunding Database:

Inspect the four CSV files and create an ERD (Entity-Relationship Diagram) of the tables using QuickDBD.
Based on the ERD, create a table schema for each CSV file, specifying data types, primary keys, foreign keys, and other constraints.
Save the database schema as a Postgres file named crowdfunding_db_schema.sql and store it in your GitHub repository.
Create a new Postgres database named crowdfunding_db.
Using the database schema, create the tables in the correct order to handle foreign keys.
Verify the table creation by running a SELECT statement for each table.
Import each CSV file into its corresponding SQL table.
Verify that each table has the correct data by running a SELECT statement for each.

By completing these steps, you will have successfully transformed the data and created the Crowdfunding Database, ready for further analysis and exploration. Make sure to document your progress and results thoroughly in your GitHub repository.
