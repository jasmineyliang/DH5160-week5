# Mini Project: Data Analysis with Pandas

## Objective
Analyze and manipulate a randomly generated DataFrame using the `pandas` library. This project will cover DataFrame creation, basic operations, filtering, aggregation, handling missing data, and visualizations.

## Steps

### 1. Setup
Install and import the necessary libraries.

```python
# Install pandas if not already installed
# pip install pandas

import pandas as pd
import matplotlib.pyplot as plt
```

### 2. Create DataFrame
Generate a random DataFrame using `pd.util.testing.makeDataFrame()`.

```python
df = pd.util.testing.makeDataFrame()
print(df.head())
```

### 3. Basic Information
Display basic information about the DataFrame.

```python
print(df.info())
print(df.describe())
```

### 4. DataFrame Manipulation
Perform the following manipulations:

1. **Add a New Column**: Add a new column 'E' which is the sum of columns 'A' and 'B'.
2. **Filter Rows**: Filter rows where column 'A' is greater than 0.
3. **Sort DataFrame**: Sort the DataFrame based on column 'C' in descending order.

```python
df['E'] = df['A'] + df['B']
filtered_df = df[df['A'] > 0]
sorted_df = df.sort_values(by='C', ascending=False)

print(df.head())
print(filtered_df.head())
print(sorted_df.head())
```

### 5. Handle Missing Data
Introduce missing data and handle it:

1. **Introduce Missing Data**: Randomly set some values in column 'B' to NaN.
2. **Handle Missing Data**: Fill missing values with the mean of column 'B'.

```python
import numpy as np

# Introduce missing data
df.loc[df.sample(frac=0.1).index, 'B'] = np.nan
print(df.head())

# Handle missing data
df['B'].fillna(df['B'].mean(), inplace=True)
print(df.head())
```

### 6. Data Aggregation
Perform data aggregation:

1. **Group By**: Group by a specific condition on column 'A' (e.g., positive or negative values) and calculate the mean for each group.
2. **Aggregation**: Calculate the sum of each column.

```python
df['A_positive'] = df['A'] > 0
grouped_df = df.groupby('A_positive').mean()
column_sum = df.sum()

print(grouped_df)
print(column_sum)
```

### 7. Visualization
Create a simple plot using the data:

1. **Plot**: Plot the values of columns 'A' and 'C'.
2. **Histogram**: Plot a histogram of column 'A'.

```python
df[['A', 'C']].plot(title='Line plot of A and C')
plt.show()

df['A'].hist(bins=20, title='Histogram of A')
plt.show()
```

### 8. Export Data
Export the manipulated DataFrame to a CSV file.

```python
df.to_csv('manipulated_data.csv', index=False)
```

## Summary
This project involves creating a DataFrame, performing various data manipulations, handling missing data, aggregating data, and visualizing it. By completing this project, you'll gain practical experience in using pandas for data analysis.

