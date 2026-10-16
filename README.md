# Air Quality Dataset

## Project Overview

This project uses the `AirQualityUCI.csv` dataset, which contains hourly
air-quality measurements and weather information collected in an Italian
city. It can be used for beginner-level data analysis, data cleaning,
and visualization with Python.

## Dataset File

-   **File:** `AirQualityUCI.csv`
-   **Format:** CSV
-   **Main fields:** Date, Time, carbon monoxide (CO), non-methane
    hydrocarbons (NMHC), benzene (C6H6), nitrogen oxides (NOx), nitrogen
    dioxide (NO2), sensor readings, temperature (T), relative humidity
    (RH), and absolute humidity (AH).

## Requirements

Install Python, then install the libraries used for analysis:

``` bash
pip install pandas numpy matplotlib seaborn
```

## How to Use in VS Code

1.  Create a project folder.
2.  Place `AirQualityUCI.csv` and this `README.md` in that folder.
3.  Open the folder in Visual Studio Code.
4.  Create a Python file, for example `main.py`.
5.  Load the CSV with pandas:

``` python
import pandas as pd

data = pd.read_csv("AirQualityUCI.csv", sep=";", decimal=",")
print(data.head())
print(data.info())
```

**Note:** If the file is comma-separated rather than semicolon-separated
in your copy, use `pd.read_csv("AirQualityUCI.csv", decimal=",")`
instead. Check the file's delimiter if the columns do not load
correctly. The original dataset may contain missing-value markers such
as `-200`; these should be handled during data cleaning.

## Suggested Analysis

-   Display the first and last rows.
-   Check column names, data types, and missing values.
-   Clean missing or invalid measurements.
-   Convert the `Date` and `Time` columns into a datetime value.
-   Calculate summary statistics for pollutant measurements.
-   Plot pollutant trends over time.
-   Compare pollutant levels with temperature and humidity.

## Example: Quick Data Inspection

``` python
import pandas as pd

data = pd.read_csv("AirQualityUCI.csv", sep=";", decimal=",")
print("First five rows:")
print(data.head())

print("\nDataset shape:")
print(data.shape)

print("\nMissing values in each column:")
print(data.isnull().sum())
```

## Important Notes

-   Confirm the separator and decimal format before analyzing the data.
-   Some columns may be empty or unnamed and may need to be removed.
-   In this dataset, `-200` is commonly used as a missing-value code for
    measurement fields; treat it as missing where appropriate.
-   This README describes the dataset and suggested workflow; it does
    not include analysis results.

## Learning Objectives

-   Practice importing CSV files with pandas.
-   Learn basic data inspection and cleaning.
-   Create visualizations using Matplotlib or Seaborn.
-   Explore relationships between air pollution and weather conditions.
