# Real Estate Data Cleaning and Transformation using SQL for Nashville Housing

---

### Table of Contents

- [Executive Summary](#executive-summary)
- [Business Problem](#business-problem)
- [Methodology](#methodology)
- [Data](#data)
- [Skills](#skills)
- [Results and Business Recommendation](#results-and-business-recommendation)
- [Project Files](#project-files)
- [How To Run](#how-to-run)
- [Next Steps](#next-steps)
- [License](#license)
- [Author Info](#author-info)

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Executive Summary

This project cleaned and transformed **56,000+ housing records** from Nashville’s open data portal to prepare them for real estate analytics and BI reporting. The challenge was that raw datasets were riddled with duplicates, missing addresses, inconsistent formats, and vague categorical values. The solution applied SQL techniques — from string parsing to window functions — to recover 2,000+ missing values, normalize addresses, and remove 800+ duplicates. The result is a reliable, structured dataset that can feed into dashboards or predictive models for property pricing and neighborhood insights. Next steps include integrating geospatial data and tax records for richer market analysis.

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Business Problem

Real estate firms, city planners, and BI teams often face poor-quality housing datasets. Inconsistent addresses make it difficult to map trends by neighborhood, missing sales data limits revenue forecasts, and duplicates inflate metrics. For Nashville, these issues prevent stakeholders from accurately tracking property sales, pricing trends, and zoning patterns. The business problem here was to make the raw data trustworthy enough to support **property valuation models, housing market dashboards, and policy analysis.**

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Methodology

The project followed a structured SQL-based cleaning pipeline:
1. **Exploration** – Identified nulls, duplicates, and inconsistent formatting.
2. **Standardization** – Converted sale dates into consistent formats and normalized categorical fields like `SoldAsVacant`.
3. **Feature Engineering** – Extracted structured fields (`Address`, `City`, `State`) from unstructured address strings using string functions.
4. **De-duplication** – Applied `ROW_NUMBER()` with `PARTITION BY` logic to detect and eliminate ~800 duplicate rows.
5. **Column Optimization** – Removed redundant columns after transformation to reduce noise and improve usability.

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Data

- **Source**: Public dataset from [Nashville’s Open Data Portal](https://data.nashville.gov/)
- **Description**:
  - Key columns: `ParcelID`, `SaleDate`, `PropertyAddress`, `OwnerAddress`, `SoldAsVacant`, `SalePrice`, `LegalReference`
  - Size: ~56,000+ records with multiple duplicates, nulls, and inconsistent address formats

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Skills

- **SQL (T-SQL):**
   - Window functions (`ROW_NUMBER()`) for duplicate detection
   - String functions (`SUBSTRING()`, `PARSENAME()`) for parsing addresses
   - Conditional logic (`CASE`) to normalize categorical values
   - Joins & subqueries to recover missing addresses
- **Data Cleaning & Transformation:** Null handling, type conversions, standardization
- **SQL Server Management Studio (SSMS):** Query execution and validation

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Results and Business Recommendation

- Recovered **~2,000 missing property addresses**, improving dataset completeness.
- Standardized all `SoldAsVacant` entries from messy Y/N labels to consistent Yes/No values.
- Removed **~800 duplicate rows**, reducing risk of inflated KPIs in BI dashboards.
- Extracted structured address fields to enable geographic and neighborhood-level analysis.

**Recommendation:** With a clean dataset, Nashville housing stakeholders can now create dashboards to monitor **property value trends, sales activity, and neighborhood development**. This foundation also supports **predictive analytics** for real estate investment and city planning.

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Project Files

The following are the files in this project: 

- [Nashville Housing Data](data/NashvilleHousingDataforDataCleaning.xlsx)
- [Nashville Housing Data Project Queries](NashvilleHousingQueries.sql)

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

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

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Next Steps

If extended, this project could:
- Enrich the dataset with **geospatial data** to allow mapping and spatial analysis.
- Integrate **tax assessment records** for more accurate valuation models.
- Build a **Power BI dashboard** on top of the cleaned dataset for real-time housing insights.
- Automate the cleaning process into an **ETL pipeline**, ensuring ongoing data quality as new sales records are published.

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

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

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)

---

## Author Info

- Github - [Github Profile](https://github.com/prasanna-sriram)
- LinkedIn - [Prasanna Sriram](https://www.linkedin.com/in/prasanna-sriram/)
- Tableau - [Tableau Public Profile](https://public.tableau.com/app/profile/prasanna.sriram.ps)

[Back to the Top](#real-estate-data-cleaning-and-transformation-using-sql-for-nashville-housing)