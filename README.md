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
4. Examines bar coupons by comparing acceptance rates for different bar-visit frequencies and driver groups, including groups defined by age, passengers, and marital status.
5. Performs an independent exploration of carry-out coupons, comparing acceptance across selected driver groups.
6. Uses Seaborn plots to explore coupon counts and customer characteristics, including income categories across occupations.

Acceptance rates are calculated from the binary `Y` column: its mean is the fraction of observations with `Y = 1`. The notebook visualizes comparisons with bar charts and subplots. Income is recorded in ranges, so charts of income by occupation should be interpreted as category comparisons rather than continuous income distributions.

## Exploratory observations

The notebook's recorded results show:

- Overall bar-coupon acceptance was about **41.0%** (827 accepted out of 2,017 bar-coupon observations).
- Among bar-coupon observations, acceptance was **37.1%** for drivers reporting three or fewer bar visits per month and **76.9%** for those reporting more than three visits.
- Drivers who visited bars more than once a month and were over 25 had a **62.2%** acceptance rate, compared with **55.4%** for all others.
- Drivers who visited bars more than once a month, were not traveling with a child, and were outside the farming, fishing, and forestry occupation group had a **62.3%** acceptance rate, compared with **54.6%** for all others.
- Overall acceptance of carry-out coupons was about **73.5%** (1,760 accepted out of 2,393 observations). Within this coupon group, acceptance was **74.0%** for drivers who reported three or fewer carry-out visits per month and **69.6%** for those reporting more than three.
- One carry-out comparison (more than one carry-out visit per month and over age 41 versus all others) showed similar rates: **56.6%** and **56.9%**, respectively.

These are descriptive results from the notebook, not causal conclusions. The carry-out comparisons also show that frequency patterns differ by group definition; frequent visits do not consistently correspond to higher acceptance.

## Running the notebook

Open `prompt.ipynb` in Jupyter Notebook or JupyterLab and run the cells in order. Keep the notebook in this directory so its relative path to `data/coupons.csv` resolves correctly.
