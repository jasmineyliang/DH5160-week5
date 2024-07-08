Sure, here's the same list formatted in Markdown with code snippets:

```markdown
# Pandas Library Understanding - Easy Questions

1. **DataFrame Creation**
   - How do you create a DataFrame from a dictionary with lists?
   ```python
   import pandas as pd

   data = {'column1': [1, 2, 3], 'column2': [4, 5, 6]}
   df = pd.DataFrame(data)
   ```

2. **DataFrame Basic Operations**
   - How do you display the first five rows of a DataFrame?
   ```python
   df.head()
   ```

3. **DataFrame Column Selection**
   - How do you select a specific column from a DataFrame?
   ```python
   df['column1']
   ```

4. **DataFrame Row Selection**
   - How do you select a row by index from a DataFrame?
   ```python
   df.iloc[0]
   ```

5. **Filtering Data**
   - How do you filter rows in a DataFrame based on a condition?
   ```python
   df[df['column1'] > 1]
   ```

6. **Adding Columns**
   - How do you add a new column to an existing DataFrame?
   ```python
   df['column3'] = [7, 8, 9]
   ```

7. **Data Aggregation**
   - How do you calculate the mean of a specific column in a DataFrame?
   ```python
   df['column1'].mean()
   ```

8. **Handling Missing Data**
   - How do you drop rows with missing values from a DataFrame?
   ```python
   df.dropna()
   ```

9. **Data Sorting**
   - How do you sort a DataFrame by a specific column?
   ```python
   df.sort_values(by='column1')
   ```

10. **Merging DataFrames**
    - How do you merge two DataFrames on a common column?
    ```python
    df1 = pd.DataFrame({'key': ['A', 'B', 'C'], 'value1': [1, 2, 3]})
    df2 = pd.DataFrame({'key': ['A', 'B', 'D'], 'value2': [4, 5, 6]})
    merged_df = pd.merge(df1, df2, on='key')
    ```
```
