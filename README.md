# Which factors are linked to stroke? A small statistics project in Python

A beginner project analysing a public stroke dataset with Python, pandas and statistics.

## Question
In this dataset, which factors (age, hypertension, heart disease, blood glucose, BMI, smoking) are linked to having a stroke? Do men and women show a different pattern?

## Data
Stroke Prediction Dataset (public, from Kaggle). 5110 people, 12 columns. The data file is **not included** in this repository. Download `healthcare-dataset-stroke-data.csv` from Kaggle and place it in the same folder as the notebook.

## What I did
1. Loaded and checked the data (size, missing values, class balance).
2. Cleaned it: removed the id column, one "Other" gender row, and rows with missing BMI (202 rows removed, 4908 left, 209 stroke cases).
3. Compared groups with summary tables and charts.
4. Ran Mann-Whitney U tests (numeric columns) and chi-square tests (category columns).
5. Fitted a logistic regression and reported odds ratios with 95% confidence intervals.
6. Compared men and women inside three age groups.

## Main findings
- Age is the strongest factor: about 2x higher odds of stroke for every 10 extra years (OR about 2.0, 95% CI 1.78 to 2.24).
- Hypertension (OR about 1.7) and higher glucose (about 5% higher odds per 10 mg/dL) are also linked, after adjusting for the other factors.
- Heart disease and current smoking point the same way, but their confidence intervals include 1, so the evidence is not clear.
- BMI, gender and rural or urban residence show no clear link. Men and women show a similar pattern in every age group.

## Limitations
- Association, not cause: one snapshot in time.
- Only 209 stroke cases, so estimates are uncertain.
- 202 rows removed, mostly missing BMI.
- About 30% of smoking status values are "Unknown".
- The original source of the dataset is not clearly documented, so this is practice and not medical evidence.
- No prediction model was built or tested.

## How to run
1. Install Anaconda and open Jupyter Notebook.
2. Put `stroke_analysis.ipynb` and `healthcare-dataset-stroke-data.csv` in one folder.
3. Open the notebook and choose Kernel, then Restart & Run All.

Libraries: pandas, numpy, matplotlib, seaborn, scipy, statsmodels.

## About this project
I built this while learning Python and statistics. I used an AI assistant (Claude) to help with the code and the structure, and I ran and read every step myself.
