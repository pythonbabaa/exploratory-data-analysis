# Data Analysis and Visualization Project

## Overview
This project demonstrates basic data analysis and visualization techniques using Python libraries such as **NumPy**, **Pandas**, **Seaborn**, and **Matplotlib**. The code is designed to perform data cleaning, transformation, querying, and visualization to extract meaningful insights from a dataset.

## Features
- **Data Inspection:** Display top/bottom rows (`.head()`, `.tail()`), descriptive stats (`.describe()`), data info (`.info()`), and column data types (`.dtypes`).
- **Data Cleaning:** Drop columns/rows, reset indices, rename columns/indices, detect/drop duplicates, handle missing values via interpolation or removal.
- **Data Analysis:** Query data, group by features with aggregate functions, analyze shape, size, count, and correlations.
- **Data Visualization:** Generate boxplots (`purchase_power`) and heatmaps for correlations.

## Installation and Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/repository-name.git
   cd repository-name
   pip install -r requirements.txt
/home/a/Desktop/user_data.csv
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
user_data = pd.read_csv('/home/a/Desktop/user_data.csv')
user_data = user_data.drop(['user_ID', 'user_level'], axis=1)
user_data = user_data.rename(columns={'first_order_month': 'first_month_order'})
sns.boxplot(x=user_data['purchase_power'])
plt.figure(figsize=(20,10))
c = user_data.corr()
sns.heatmap(c, cmap='BrBG', annot=True)

