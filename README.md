
<h1 align="center"> Amazon Data Related Books - Transformation Phase </h1>

<p align="center">
<img  src="https://github.com/user-attachments/assets/1f021b3e-c98e-4cca-b440-08e693ac6ead">
</p>

<p align="center">
Below are images showing the dataset before and after the data cleaning process.
</p>

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/1eacab1c-4a6b-4eaa-b768-d1f6197effcb" alt="Before Data Cleaning" height="300" width="auto" style="display: block;"/> <p style="text-align: center;">Before Data Cleaning</p> </td>
    <td><img src="https://github.com/user-attachments/assets/b2993dff-4c0b-423f-b2c7-4c9efd1190bb" alt="After Data Cleaning" height="300" width="auto" style="display: block;"/>
     <p style="text-align: center;">After Data Cleaning</p>
    </td>
  </tr>
</table>


### Project Overview

This project involves transforming a dataset of Amazon data-related book information as part of an ETL (Extract, Transform, Load) process. The main focus was on cleaning and standardising the data to prepare it for analysis. The transformations include renaming headers, cleaning attribute values, replacing NaN values, and changing data types of various attributes.

[Click to view code ](https://github.com/TendaiPhikiso/Amazon_web_Scraping_Transformation/blob/main/Amazon%20web%20scraping%20-%20Transformation%20Phase.ipynb)

 ### Data Transformation Steps

| Step                   | Description                                                                                             | Example                                                          |
|------------------------|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| **1. Renaming Headers**| The headers of the dataset have been renamed to be more descriptive and consistent. This helps in making the data more understandable and easier to work with. | - **Name** column was changed to **AuthorName**. |
| **2. Cleaning Attribute Values** | Certain columns contained values that needed cleaning to make the data consistent. | - **ReviewCount**: Removed the word "ratings" and commas from numeric values. |
| **3. Replacing NaN Values** | NaN values in the dataset were replaced with appropriate default values.                              | - **AuthorName**: Replaced NaN with "Unknown".<br>- **SellingPrice**: Replaced NaN with 0. |
| **4. Changing Data Types**  | Data types of columns were changed to ensure consistency and correctness.                            | - **PrintLength**: Converted to `int`.<br>- **Rating**: Converted to `float` after handling non-numeric values. |



[Click to view cleaned data ](https://github.com/TendaiPhikiso/Amazon_web_Scraping_Transformation/blob/main/cleaned-data.csv)


### Next Steps
<p align="center">
<img  src="https://github.com/user-attachments/assets/2fdd6687-cc13-4819-94f4-18483cf694b2">
  Photo by sarasanalytics.com
</p>

1. **Loading Data**: The next step involves loading the cleaned data into a Microsoft SQL Server database. This will enable efficient querying and analysis of the data.

2. **View Extract Phase**: If you are interested in viewing the details of the Extract phase of the project, you can find it [here](https://github.com/TendaiPhikiso/Amazon_web_Scraping).


