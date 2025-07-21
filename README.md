# Nashville Housing Data Cleaning with SQL

---

### Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Data](#data)
- [Approach](#approach)
- [Tools And Technologies](#tools-and-technologies)
- [Project Files](#project-files)
- [Project Outcome](#project-outcome)
- [How To Run](#how-to-run)
- [Conclusion](#conclusion)
- [License](#license)
- [Author Info](#author-info)

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Overview
This project focuses on **cleaning and transforming raw housing data from Nashville** using SQL. The aim is to prepare the dataset for accurate analysis by handling nulls, standardizing formatting, extracting structured information, and removing duplicates. These techniques are critical in real estate analytics, BI reporting, and data engineering pipelines where clean and structured data is foundational.

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Problem Statement
Raw real estate datasets often contain incomplete, duplicated, or inconsistently formatted information. This compromises downstream analysis, KPIs, and dashboard accuracy. This project addresses these common data quality issues by applying SQL-based data cleaning techniques to ensure the dataset is reliable for analysis and business intelligence reporting.

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Data
- **Source**: Public dataset from [Nashville’s Open Data Portal](https://data.nashville.gov/)
- **Description**:
  - Key columns: `ParcelID`, `SaleDate`, `PropertyAddress`, `OwnerAddress`, `SoldAsVacant`, `SalePrice`, `LegalReference`
  - Size: ~56,000+ records with multiple duplicates, nulls, and inconsistent address formats

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Approach
1. **Data Exploration and Cleaning**
   - Checked for nulls, duplicates, and data type issues
   - Added `SaleDateConverted` column to store standardized sale dates
   - Replaced missing `PropertyAddress` values using matching `ParcelID` records
2. **Feature Engineering**
   - Split `PropertyAddress` and `OwnerAddress` into `Address`, `City`, and `State` using `SUBSTRING()` and `PARSENAME()`
   - Standardized `SoldAsVacant` values from `Y/N` to `Yes/No`
3. **Duplicate Handling**
   - Used `ROW_NUMBER()` with `PARTITION BY` to identify and filter out duplicate records
4. **Column Optimization**
   - Dropped original address columns after successful transformation to reduce clutter

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Tools and Technologies
- Microsoft SQL Server
- T-SQL (subqueries, joins, CTEs, window functions, string parsing)
- SQL Server Management Studio (SSMS)
- Git & GitHub for version control

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Project Files

The following are the files in this project: 

- [Nashville Housing Data](data/NashvilleHousingDataforDataCleaning.xlsx)
- [Nashville Housing Data Project Queries](NashvilleHousingQueries.sql)

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Project Outcome

- Recovered ~2,000 missing `PropertyAddress` values using `ParcelID` matching
- Successfully split and extracted structured address components from combined fields
- Converted all `SoldAsVacant` entries into consistent "Yes"/"No" format
- Identified and prepared ~800 duplicate rows for deletion using a window function
- Reduced dimensionality by dropping unnecessary columns post-cleaning

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/prasanna-sriram/nashville-housing-data.git

2. Go to the project directory

    ```bash
    cd covid19-global-data-analysis
    ```

3. Open NashvilleHousingQueries.sql in SQL Server Management Studio (SSMS)

4. Run the queries on the provided Nashville Housing table

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Conclusion

This project highlights the power of SQL in cleaning and restructuring messy real-world data — a foundational skill in data analytics, business intelligence, and data engineering. Cleaned data is now ready for deeper insights such as property pricing trends, neighborhood analysis, or Power BI dashboarding. Future enhancements could include geospatial enrichment or integrating additional datasets such as tax records.

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## License

MIT License

Copyright (c) [2025] [Prasanna Sriram]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[Back to the Top](#nashville-housing-data-cleaning-with-sql)

---

## Author Info

- Github - [Github Profile](https://github.com/prasanna-sriram)
- LinkedIn - [Prasanna Sriram](https://www.linkedin.com/in/prasanna-sriram/)
- Tableau - [Tableau Public Profile](https://public.tableau.com/app/profile/prasanna.sriram.ps)

[Back to the Top](#nashville-housing-data-cleaning-with-sql)