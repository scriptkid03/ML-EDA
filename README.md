# GenZ Survey Data Documentation

## Overview

This dataset contains survey responses from GenZ individuals regarding their app usage, satisfaction levels, and demographics. The data was cleaned and standardized for consistency and analysis.

## Data Dictionary

| Column Name        | Data Type | Description                                           |
| ------------------ | --------- | ----------------------------------------------------- |
| `Age`              | Integer   | Age of the respondent.                                |
| `Gender`           | Category  | Gender of the respondent (e.g., Male, Female, Other). |
| `Primary_App`      | Category  | The main app used daily.                              |
| `Secondary_Apps`   | Category  | Other frequently used apps.                           |
| `Daily_Usage_Time` | Integer   | Time spent on the primary app daily (in minutes).     |
| `Satisfaction`     | Integer   | Satisfaction level (scale of 1-10).                   |

## Data Cleaning Steps

1. **Handled Missing Values:**

   - Replaced missing values with `"unknown"` for consistency.

2. **Removed Duplicates:**

   - Checked and confirmed no duplicate rows were present.

3. **Standardized Categorical Data:**

   - Converted all text values to lowercase for uniformity.

4. **Converted Categorical Columns to 'Category' dtype:**

   - Optimized memory usage by converting categorical columns.

5. **Converted Time to Numeric:**

   - Mapped daily usage time to minutes.

6. **Outlier Detection:**
   - Checked `Age`, `Satisfaction`, and `Daily_Usage_Time` using the IQR method. No extreme outliers were found.

## Collaboration & Versioning

- The dataset and documentation are tracked using GitHub.
- Changes are committed with meaningful messages for version control.
