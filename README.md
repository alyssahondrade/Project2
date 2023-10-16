# Crowdfunding_ETL
Project 2 - UWA/edX Data Analytics Bootcamp

Github repository at: [https://github.com/alyssahondrade/Crowdfunding_ETL.git](https://github.com/alyssahondrade/Crowdfunding_ETL.git)

## Table of Contents
1. [Introduction]
    1. [Goal]
    2. [Repository Structure]
    3. [Dataset]
2. [Approach]
3. [References]


## Introduction

### Goal
-- project goal here --

### Repository Structure
`Resources` directory contains:
- [`crowdfunding.xlsx`](https://github.com/alyssahondrade/Crowdfunding_ETL/blob/main/Resources/crowdfunding.xlsx)
- [`campaign.csv`](https://github.com/alyssahondrade/Crowdfunding_ETL/blob/main/Resources/campaign.csv)
- [`category.csv`](https://github.com/alyssahondrade/Crowdfunding_ETL/blob/main/Resources/category.csv)
- [`contacts.csv`](https://github.com/alyssahondrade/Crowdfunding_ETL/blob/main/Resources/contacts.csv)
- [`subcategory.csv`](https://github.com/alyssahondrade/Crowdfunding_ETL/blob/main/Resources/subcategory.csv)

`ERD` directory contains:
- [`ERD_CrowdFunding.drawio`]()
- [ERD_image]

The root directory contains:
- [`ETL_Mini_Project_Group_6.ipynb`](https://github.com/alyssahondrade/Crowdfunding_ETL/blob/main/ETL_Mini_Project_Group_6.ipynb) - the source code
- [`schema.sql`](https://github.com/alyssahondrade/Crowdfunding_ETL/blob/main/schema.sql)

### Dataset
-- insert source here, refer to Project 2 BCS page --


## Approach

### Schema
Variable | Minimum Requirement | Chosen Limit
:---: | --- | ---
`category_id` | `VARCHAR(4)` since "cat1...cat9" | `VARCHAR(5)` to allow for "cat10...etc."
`subcategory_id` | `VARCHAR(8)` since "subcat1...subcat9" | `VARCHAR(10)` to allow for "cat100...etc."
`first_name` | `VARCHAR(12)` since "Michelangelo" | `VARCHAR(30)` to allow for longer names
`last_name` | `VARCHAR(13)` since "Montanariello" | `VARCHAR(30)` to allow for longer names
`email` | The longest email required `VARCHAR(42)` | `VARCHAR(60)` to account for longer emails
`company_name` | The longest company name required `VARCHAR(33)` | Rounded up to `VARCHAR(50)`
`description` | The longest description required `VARCHAR(53)` | Rounded up to `VARCHAR(75)`
`goal` & `pledged` | The value with maximum digits required `FLOAT(7)` | Rounded up to `FLOAT(10)`
`outcome` | The longest option "successful" required `VARCHAR(10)` | Retained, since not expecting new options
`country` | All country abbreviations required `VARCHAR(2)` | Retained, to ensure consistency and integrity of data
`currency` | All currency abbreviations required `VARCHAR(3)` | Retained, for the same reasons as `country`

-- describe approach here --

-- insert image of the ERD here, after describing ERD creation process --


## References
- [1] SQL Data Types [http://www.cs.toronto.edu/~nn/csc309/guide/pointbase/docs/html/htmlfiles/dev_datatypesandconversionsFIN.html](http://www.cs.toronto.edu/\~nn/csc309/guide/pointbase/docs/html/htmlfiles/dev_datatypesandconversionsFIN.html)

- [2] How to display table in README.md file in Github? [https://stackoverflow.com/questions/39378020/how-to-display-table-in-readme-md-file-in-github](https://stackoverflow.com/questions/39378020/how-to-display-table-in-readme-md-file-in-github)
