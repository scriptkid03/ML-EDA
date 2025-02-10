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

## Exploratory Data Analysis (EDA)

### Key Findings:

- **Gender Differences:** Certain dating apps were more popular among specific genders.
- **Age-Based Trends:** Users aged 18-24 spent the most time on dating apps.
- **Urban vs. Rural Patterns:** Urban users showed higher engagement compared to rural users.
- **Multiple App Usage:** A significant number of users were active on multiple dating apps.

## Feature Engineering

- **Encoded categorical variables** using Label Encoding.
- **Normalized numerical variables** using MinMaxScaler.
- **Created `Active_App_Count` feature** based on the number of apps used per user.

## Future Improvements

- Incorporate geospatial analysis if location data is more detailed.
- Analyze the impact of user satisfaction on engagement levels.
- Consider time-series modeling to observe trends over different periods.

## GitHub Workflow

- **Branching:** `feature-EDA` was created for exploratory analysis.
- **Pull Requests:** Opened for team feedback before merging.
- **Final Merge:** All analysis and feature engineering updates were merged into `main`.

## Summary

This project provides insights into Gen-Z dating behavior and prepares the dataset for predictive modeling. The structured documentation ensures ease of collaboration and future extensions.
