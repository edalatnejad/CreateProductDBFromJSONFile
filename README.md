# CreateProductDBFromJSONFile
This repository contains an SSIS project named CreateProductDbFromJSON. The project is designed to read and deserialize a JSON file using Newtonsoft.Json library. The JSON file used in this project is sourced from Flipkart, an E-commerce website, and was downloaded from Kaggle.

Dataset Information 

The dataset includes the following fields:
* _id
* pid
* title
* original_price
* crawled_at
* description
* out_of_stock
* images (It is a list of product image URLs)
* product_details(It includes product details, which are of dictionary type.)
* discount
* brand
* seller_name
* seller_rating
* url
* flipkart_assured
* breadcrumbs


The CreateProductDbFromJSON package aims to create a relational database and load a json file in three table:

* **Product**
    * ProductId
    * PId
    * Name
    * Price
    * Category
    * SubCategory
    * Brand
    * CrawledAt
    * Description
    * OutOfStock
    * Url
* **ProductDetails**
    * ProductId
    * KeyName
    * KeyValue
* **ProductImages**
    * ProductId
    * ImageURL
      
The SSIS project reads the JSON file, parses its contents, and loads the data into the ProductDB database. The data is organized into the above-mentioned tables to maintain relational integrity and facilitate efficient querying.

# Dependencies
   * SQL Server: The project requires a SQL Server instance to create and populate the ProductDB database.
   * SQL Server Data Tools (SSDT)
   * Visual Studio & VSTA
   * Sql Server Integration Service
   * Newtonsoft.Json library
     
#  Setting up and Running SSIS Package
* Ensure that you have SQL Server installed and running.
* Create a new database named ProductDB in your SQL Server instance usin **Create database ProductDB** 
* All tables and keys will be created in the SSIS package.
* Open the CreateProductDbFromJSON solution in Visual Studio or SSDT (SQL Server Data Tools).
* Configure the SSIS package to point to the JSON file location and specify the SQL Server connection details using **variable tab**.
* Run the SSIS package to populate the ProductDB database with data from the JSON file.

Feel free to explore, modify, and utilize the SSIS package according to your requirements. If you encounter any issues or have suggestions for improvement, please feel free to open an issue or submit a pull request. Your contributions are highly appreciated!
