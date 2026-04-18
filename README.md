# practical10

Aim : study of panda

Pandas is an essential, open-source Python library for data analysis and manipulation.

1. Data Exploration & Inspection
Before performing operations, you need to understand the "health" of your dataset.

df.info(): The first command you should run. It shows the number of non-null entries and memory usage.

df.describe(): Generates descriptive statistics (mean, std, min, max, quartiles) for all numerical columns.

df.head(n) / df.tail(n): Views the first or last n rows to check for data alignment.

df.nunique(): Counts unique values in each column—essential for identifying categorical vs. continuous data.

2. Handling Missing Data (Data Cleaning)
Real data is rarely perfect. Pandas provides tools to manage "NaN" (Not a Number) values.

df.isnull().sum(): Returns the count of missing values per column.

df.dropna(): Removes rows or columns with missing values.

df.fillna(value): Replaces missing values with a specific number or the mean/median to keep the dataset size intact.

3. Advanced Data Manipulation
Grouping and Aggregation

This is the "Power User" feature of Pandas, often called the Split-Apply-Combine strategy.

df.groupby('ColumnName').mean(): Groups data by a category and calculates the average for each group.

df.groupby('ColumnName').agg(['min', 'max', 'sum']): Performs multiple different calculations at once on grouped data.

Sorting

df.sort_values(by="ColumnName", ascending=False): Reorders your data based on specific criteria.

4. Merging and Joining
Rarely do we work with just one table. Pandas handles relational data like SQL does.

5. Element-wise Operations & Transformation
If you need to modify every value in a column:

df["Col"].apply(lambda x: x + 10): Applies a custom function to every element in a column.

df["Col"].map({old_val: new_val}): Great for replacing categorical labels (e.g., changing "M/F" to "Male/Female").

df.rename(columns={"OldName": "NewName"}): Changes the column headers.

6. Time Series Analysis
Pandas is famous for its ability to handle dates and times efficiently.

pd.to_datetime(): Converts a string column (like "2023-01-01") into actual Python datetime objects.

df.resample('M').mean(): If your index is time-based, this allows you to "downsample" data (e.g., turning daily data into monthly averages).

Function	Purpose
pd.concat()	Glues two DataFrames together (either vertically or horizontally).
pd.merge()	Joins two DataFrames based on a common key (Inner, Outer, Left, Right joins).
df.join()	Joins DataFrames based on their index labels.

Conclusion: > The Pandas library provides a robust ecosystem for the entire data lifecycle: from ingestion (reading CSVs/SQL) and cleaning (handling nulls) to transformation (grouping/merging) and statistical analysis. By utilizing the DataFrame structure, users can perform complex vectorised operations that are significantly faster and more readable than standard Python loops.
