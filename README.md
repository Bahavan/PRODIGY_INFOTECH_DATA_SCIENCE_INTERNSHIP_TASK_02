# PRODIGY_INFOTECH_DATA_SCIENCE_INTERNSHIP_TASK_02

# Task-02: Exploratory Data Analysis (EDA) & Data Cleaning

## Task Description
Perform data cleaning and exploratory data analysis (EDA) on a dataset of your choice, such as the Titanic dataset from Kaggle. Explore the relationships between variables and identify patterns and trends in the data.

## Dataset
For this task, you can use the Titanic dataset from Kaggle:
[Titanic Dataset](https://www.kaggle.com/c/titanic/data)

## Instructions
1. Download the dataset from Kaggle.
2. Load the dataset using `pandas`.
3. Perform **Data Cleaning**, including:
   - Handling missing values.
   - Removing duplicates.
   - Fixing incorrect data types.
4. Conduct **Exploratory Data Analysis (EDA)**:
   - Generate descriptive statistics.
   - Visualize distributions using histograms, box plots, and pair plots.
   - Identify correlations between features.
   - Analyze relationships between variables.

## Requirements
- Python 3.x
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`

## Example Code
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load Titanic dataset
df = pd.read_csv("titanic.csv")

# Display basic info
print(df.info())

# Handle missing values
df.fillna(df.median(numeric_only=True), inplace=True)

# Visualize survival count
sns.countplot(data=df, x="Survived")
plt.title("Survival Count")
plt.show()

# Correlation heatmap
plt.figure(figsize=(10,6))
sns.heatmap(df.corr(), annot=True, cmap="coolwarm", fmt=".2f")
plt.title("Feature Correlation Heatmap")
plt.show()
