
<h1 align="center"> Amazon Data Related Books - Transform Phase </h1>

<p align="center">
<img  src="https://github.com/user-attachments/assets/1f021b3e-c98e-4cca-b440-08e693ac6ead">
</p>

### Data Quality Observations

Before performing data transformation, it’s important to assess the quality of the data to understand what needs to be cleaned. The following observations were made on the 
[amazon_dataBooks.csv](https://github.com/TendaiPhikiso/Amazon_web_Scraping/blob/main/amazon_dataBooks.csv) table:
<details>
<summary>
Click to view Observations
</summary>
  
| **Column**               | **Observation**                                                                                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Column Headers           | Most header names are not descriptive, for instance, "title" and "name," which can make it difficult to understand what the column entails.                                                                                                 |
| title                    | No issue identified within the column other than renaming the header.                                                                                                                                                                       |
| name                     | Contains 10 null values and trailing text “\n(Author)” which needs to be removed as we only want the name of the author.                                                                                                                    |
| sellingPrice             | Contains 71 null values and the £ symbol, which needs to be removed if numerical analysis is to take place in the analysis phase.                                                                                                           |
| listingPrice             | Contains 183 null values, which we can assume means other books are not discounted. It has leading text “RRP: £” and “was: £” which need to be removed as the column will be used for numeric analysis.                                      |
| typeOfBook               | Contains 9 null values, and includes a hyphen and date which should be removed to keep only the book type (e.g., Paperback, Hardcover). Column also contains additional text for Kindle Edition book type e.g "1st Edition, Kindle Edition" or "[Print Replica] Kindle Edition". There are to be removed in order to keep the txt Kindle Edition only.                                                          |
| printLength              | Contains text values "Print length," and " pages" which need to be removed to retain only the numerical values. It has 77 null values.                                                                                                      |
| publicationDate          | Contains text "Publication date: " which needs to be removed to retain only the date values. Contains 10 null values.                                                                                                                       |
| rating                   | Contains text "out of 5 stars,” which is unnecessary as we know that the ratings will be out of 5. Other rows contain text such as “Previous slide of product details” instead of the review number itself, which can cause issues when converting the column into a numeric datatype. |
| reviews                  | Contains text “ratings” as well as a comma with other numeric values that are 4 digits long.                                                                                                                                                |
| availability             | Contains 1 null value. Some entries have text value such as "Usually dispatched within 2 to 3 days"  or "Only 3 left in stock (more on the way)."                                                                                                                                                                                                                   |

</details>

### 
<p align="center">
Below are images showing the dataset before and after the data cleaning process.
</p>

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/1eacab1c-4a6b-4eaa-b768-d1f6197effcb" alt="Before Data Cleaning" height="300" width="auto" style="display: block;"/> 
     <p align="center">Before Data Cleaning</p> </td>
    <td><img src="https://github.com/user-attachments/assets/b2993dff-4c0b-423f-b2c7-4c9efd1190bb" alt="After Data Cleaning" height="300" width="auto" style="display: block;"/>
    <p align="center">After Data Cleaning</p>
    </td>
  </tr>
</table>


### Project Overview

This project involves transforming a dataset of Amazon data-related book information as part of an ETL (Extract, Transform, Load) process. The main focus was on cleaning and standardising the data to prepare it for analysis. The transformations include renaming headers, cleaning attribute values, replacing NaN values, and changing data types of various attributes.

[Click to view code ](https://github.com/TendaiPhikiso/Amazon_web_Scraping_Transformation/blob/main/Amazon%20web%20scraping%20-%20Transformation%20Phase.ipynb)


## Data Transformation Steps

| Step                       | Description                                                                                             | Example                                                          |
|----------------------------|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| **1. Renaming Headers**    | The headers of the dataset have been renamed to be more descriptive and consistent. This helps in making the data more understandable and easier to work with. | - **Name** column was changed to **AuthorName**. |
| **2. Cleaning Attribute Values** | Certain columns contained values that needed cleaning to make the data consistent. | - **ReviewCount**: Removed the word "ratings" and commas from numeric values. |
| **3. Replacing NaN Values** | NaN values in the dataset were replaced with appropriate default values.                              | - **AuthorName**: Replaced NaN with "Unknown".<br>- **SellingPrice**: Replaced NaN with 0. |
| **4. Changing Data Types** | Data types of columns were changed to ensure consistency and correctness.                            | - **PrintLength**: Converted to `int`.<br>- **Rating**: Converted to `float` after handling non-numeric values. |
| **5. Removing Duplicate Rows** | Duplicate rows in the dataset were identified and removed to ensure data integrity.              | - Total number of duplicate rows found: **130**. |


<p align="center">
  Duplicate rows Img
  
<img  src="https://github.com/user-attachments/assets/82f2588c-2778-4390-8db9-1f3b649dbc05">
</p>


[Click to view cleaned data ](https://github.com/TendaiPhikiso/Amazon_web_Scraping_Transformation/blob/main/cleaned-data.csv)


### Next Steps
<p align="center">
<img  src="https://github.com/user-attachments/assets/2fdd6687-cc13-4819-94f4-18483cf694b2">
  Photo by sarasanalytics.com
</p>

1. **Loading Data**: The next step involves loading the cleaned data into a Microsoft SQL Server database. This will enable efficient querying and analysis of the data.

2. **View Extract Phase**: If you are interested in viewing the details of the Extract phase of the project, you can find it [here](https://github.com/TendaiPhikiso/Amazon_web_Scraping).


