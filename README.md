# Required-Assignment-5.1-Will-the-Customer-Accept-the-Coupon-
Module 5: Practical Application 1

# Assignment 5.1: Will the Customer Accept the Coupon?

## Overview

This notebook explores which factors may be associated with a driver's decision to accept a driving coupon. The analysis uses Python, pandas, and visualizations to compare coupon acceptance across customer and driving-context groups.

## Dataset

The notebook uses `data/coupons.csv`. The survey data describes driving scenarios and customer attributes, including:

- Coupon type and acceptance (`Y`: `1` means accepted; `0` means not accepted)
- Age, gender, marital status, occupation, and income
- Passenger, weather, temperature, time, and destination
- How often the driver visits bars, coffee houses, and restaurants or gets takeout

The notebook describes the data as collected through an Amazon Mechanical Turk survey and sourced from the UCI Machine Learning Repository.

## Analysis

The notebook:

1. Loads and inspects the dataset, including its dimensions, column types, missing values, duplicate rows, and numeric summaries.
2. Handles missing data by dropping the `car` column, which has the most missing values, and filling remaining missing values with each column's most frequent value. The cleaned data is stored in `NewData`.
3. Visualizes overall coupon acceptance, coupon-type counts, and the temperature distribution.
4. Examines bar coupons by comparing acceptance rates for different bar-visit frequencies and driver groups.
5. Performs an independent exploration of carry-out coupons, comparing acceptance across selected driver groups.

Acceptance rates are calculated from the binary `Y` column: its mean is the fraction of observations with `Y = 1`. The notebook visualizes comparisons with bar charts.

## Exploratory observations

The notebook's hypothesis is that drivers who visit bars more often may be more likely to accept bar coupons. Its carry-out exploration comments also report higher acceptance for some selected groups, including more frequent carry-out customers under age 30. These are exploratory patterns in the observed data, not evidence that the characteristics cause coupon acceptance.

## Running the notebook

Open `prompt.ipynb` in Jupyter Notebook or JupyterLab and run the cells in order. Keep the notebook in this directory so its relative path to `data/coupons.csv` resolves correctly.
