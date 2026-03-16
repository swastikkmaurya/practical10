# practical10

Aim : study of panda

Pandas is an essential, open-source Python library for data analysis and manipulation.

pd.Series(): Creates a one-dimensional labeled array capable of holding any data type.

pd.DataFrame(): Creates a two-dimensional, size-mutable, and tabular data structure with labeled axes.

df.shape: An attribute that returns a tuple representing the dimensionality of the DataFrame.

df.ndim: Returns an integer representing the number of axes/dimensions.

df.columns: Returns the column labels of the DataFrame.

df.dtypes: Returns the data types of each column.

df.loc[row_index, "ColumnName"]: Accesses a group of rows and columns by labels or a boolean array.

df.iloc[row_index, col_index]: Accesses a group of rows and columns by integer-based positions.

df.drop(): Removes specified rows or columns. In the notebook, axis=1 is used to specify a column removal.

df.mean(): Calculates the average of the values in a column.

df.max(): Returns the highest value in a column.

df.min(): Returns the lowest value in a column.

df[df["Marks"] > 80]: It filters the DataFrame to show only the rows where the condition (Marks greater than 80) is true.

Conclusion:

Hence pandas library were implented in python and operations were done using them.
