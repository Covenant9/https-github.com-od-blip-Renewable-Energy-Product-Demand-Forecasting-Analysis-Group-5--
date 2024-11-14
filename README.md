# Renewable Energy Product Demand Forecasting Analysis by Group 5

---

# Renewable Product Demand Forecasting Analysis

## Contributors
- [Ifeka Odira Hillary](https://github.com/od-blip) 
- [Adebayo Deborah](https://github.com/Deborah8991?tab=projects)
- [Dr Samuel Israel](https://github.com/drsam-israel)
- [Convenant Lenu](https://github.com/Covenant9)

## Table of Contents
1. [Project Overview](#project-overview)
2. [Datasets and Data Cleaning](#datasets-and-data-cleaning)
   - [Inflation Data](#1-inflation-data)
   - [Foreign Exchange Dataset](#2-foreign-exchange-dataset)
   - [Renewable Energy Consumption Dataset](#3-renewable-energy-consumption-dataset)
3. [Data Merging and Preparation](#data-merging-and-preparation)
4. [Analysis and Forecasting](#analysis-and-forecasting)
   - [Forecasting](#forecasting)
   - [Additional Charts](#additional-charts)
5. [References](#references)

## Project Overview
This project aims to forecast the demand for renewable energy products in Nigeria by analyzing historical data on inflation, foreign exchange rates, and renewable energy consumption trends. We developed projections for future energy demands, identifying potential challenges and growth opportunities in the renewable energy sector.

## Datasets and Data Cleaning

### 1. Inflation Data
- **Objective**: Analyze how inflation impacts renewable energy consumption.
- **Steps**:
  - Loaded the dataset into Power Query.
  - Removed irrelevant columns, such as those focused on inflation in specific sectors like food, to streamline analysis.
  - Merged the "Year" and "Month" columns into a single "Date" column to facilitate time-based analysis, while retaining the "Year" column (2003–2023) for relationship building. Rows with years 2000–2002 were removed.
  - Added a new column, "Country," with the value set to "Nigeria" for easier dataset merging.
  - Checked and ensured correct data types (e.g., date for the new "Date" column, numeric for inflation rates).

### 2. Foreign Exchange Dataset
- **Objective**: Track how exchange rate fluctuations affect renewable energy costs.
- **Steps**:
  - Loaded the dataset into Power Query.
  - Retained only the black-market exchange rate columns, "Buying Rate" and "Selling Rate," as these are used by Nigerian customs.
  - Filtered the "Currency" column to include only rows with "US DOLLAR."
  - Cleaned the "Year" column, removing entries for 2000–2002 to maintain consistency with other datasets.
  - Verified and corrected data types.

### 3. Renewable Energy Consumption Dataset
- **Objective**: Assess renewable energy consumption trends and their drivers.
- **Steps**:
  - Loaded the dataset and filtered for rows where the "Country" column equals "Nigeria."
  - Removed irrelevant columns, such as "Nuclear Energy," to focus solely on renewable energy metrics.
  - Filled missing cells in the "Financial Flows" column with zero.
  - **Calculated a 3-year moving average** for relevant columns like "Renewable Energy Share" and "Electricity Share" and shaded the moving average columns in green.
  - Retained the "Year" and "Country" columns to facilitate merging with other datasets.
  - Replaced all missing numerical values with zero and verified data types.

## Data Merging and Preparation
1. **Loaded all three datasets** into Power Query for final cleaning and preparation.
2. Merged "Inflation Data" with the "Renewable Energy Consumption" dataset using "Merge Queries as New."
3. Further merged the result with the "Foreign Exchange" dataset, resulting in a comprehensive dataset covering inflation, energy consumption, and exchange rates.
4. Removed duplicate columns, such as "inflation data.year," "inflation data.Country," and "forex data.year," to maintain a clean structure.
5. Removed duplicate rows in the "Year" column for consistency.
6. Loaded the final merged dataset into Excel for analysis.

## Analysis and Forecasting

### Forecasting
- **Forecasting Method**: Used Excel's `FORECAST.ETS` function to project future data.
- **Projections**:
  - **Renewable Energy Share (2003–2030)**:
    ```excel
    =FORECAST.ETS(target_year, known_y’s, known_x’s, seasonality, [data_completion], [aggregation])
    ```
  - **Energy Consumption Per Capita**:
    ```excel
    =FORECAST.ETS(target_year, known_y’s, known_x’s, seasonality, [data_completion], [aggregation])
    ```
  - **Exchange Rate by Year**:
    ```excel
    =FORECAST.ETS(target_year, known_y’s, known_x’s, seasonality, [data_completion], [aggregation])
    ```

### Additional Charts
- **Renewable Energy Share** (annual trend analysis)
- **Financial Flows in Renewable Energy** (tracking investment growth)
- **Renewable Capacity per Capita** (monitoring individual access trends)
- **Impact of Inflation on Energy Consumption** (analyzing sensitivity to inflation)
- **Energy Consumption** (yearly trend and 3-year moving average)

## References
- [Kaggle](https://www.kaggle.com)
- [GOGLA](https://www.gogla.org)
- [Central Bank of Nigeria](https://www.cbn.gov.ng)
- [U.S. Energy Information Administration](https://www.eia.gov/renewable)
- [International Renewable Energy Agency (IRENA)](https://www.irena.org)
