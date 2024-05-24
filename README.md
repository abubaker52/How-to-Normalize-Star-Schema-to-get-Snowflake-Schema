Normalize Star Schema to Snowflake Schema

This repository provides a detailed guide on how to normalize a Star Schema into a Snowflake Schema using an Excel file as the data source and Power BI for visualization. Follow the instructions and resources below to transform your data model efficiently.
📂 Repository Contents

    📊 Excel File: The data source file containing the initial Star Schema.
    📈 Power BI File: The final Power BI file with the normalized Snowflake Schema.
    🎥 Instructional Videos: A series of videos that demonstrate the entire process step-by-step.

🛠 Prerequisites

Before you begin, ensure you have the following tools installed:

    💻 Microsoft Excel
    📊 Power BI Desktop

📋 Step-by-Step Guide
1. Load and Prepare Data

    📥 Download the Excel File: Download the Excel file from this repository.
    🏁 Open Power BI Desktop: Launch Power BI Desktop and import the Excel file.
        Go to Home > Get Data > Excel.
        Select the downloaded Excel file and load the data into Power BI.

2. Open Power Query Editor

    🔄 Open Power Query Editor: Navigate to Home > Transform Data to open the Power Query Editor.
    🧹 Prepare Data: Clean and prepare your data as needed. Remove unnecessary columns and ensure data consistency.

3. Create Sub-Dimension Tables

    🕵️ Identify Attribute Groups: Determine which attributes in your dimension tables can be split into separate, related tables.
    ✂️ Isolate Attributes: For each attribute group, create a new sub-dimension table:
        Select the dimension table and isolate the attribute group using Remove Other Columns.
        Remove duplicates by selecting Remove Duplicates.
    🏷️ Rename and Load: Rename the new sub-dimension table appropriately and load it back into Power BI.

4. Add Keys to Dimension Tables

    🔑 Add Key Columns: Add key columns in the original dimension table that correspond to each sub-dimension table:
        Use Merge Queries to join the sub-dimension table back to the original dimension table on the common attribute.
        Expand the merged table to include the key column.
    🗑️ Remove Redundant Columns: Remove the redundant attribute columns from the original dimension table, keeping only the keys.

5. Establish Relationships

    🔗 Define Relationships: In the Model view, establish relationships between your fact table and the newly created sub-dimension tables by dragging and dropping key columns.
    ✅ Verify Model: Ensure all relationships are correctly defined and validate the model for accuracy.

Example Conversion
From Star Schema:

    📊 Fact Table: Sales
    📊 Dimension Table: Products

To Snowflake Schema:

    📊 Fact Table: Sales
    📊 Dimension Tables: Products, Product Category (new), SubCategory (new)

6. Validate and Optimize

    🔍 Validate Schema: Ensure that the new Snowflake Schema is correct and all relationships are properly defined.
    🚀 Optimize Performance: Perform any necessary optimization to enhance the performance of your data model.

📚 Resources

To assist you in the process, we have prepared a series of instructional videos. These videos provide a visual guide to each step outlined above.

    🎥 https://drive.google.com/drive/folders/1NGNzCqNUTFF7BlhZ4pwUCbmrcwAf4hRL?usp=sharing

🗂 Final Result

Check the final Power BI file in this repository to see the completed Snowflake Schema.

    📈 Power BI File

📌 Conclusion

Normalizing a Star Schema to a Snowflake Schema can significantly improve your data model's efficiency and maintainability. By following this guide, you will transform your data model to leverage the benefits of a Snowflake Schema.

Feel free to open an issue if you encounter any problems or have any questions.
