# Python-Pandas-cheat-sheet
Python Pandas cheat sheet for data analysis

**Data Input/Output**

    pd.read_csv('file.csv'): Reads data from a CSV file into a DataFrame.
    pd.read_excel('file.xlsx'): Reads data from an Excel file.
    df.to_csv('output.csv', index=False): Writes DataFrame to a CSV file.
    df.to_excel('output.xlsx', index=False): Writes DataFrame to an Excel file.

**Data Exploratio**

    df.head(n): Displays the first n rows.
    df.tail(n): Displays the last n rows.
    df.info(): Provides a summary of the DataFrame, including column names, data types, and non-null counts.
    df.describe(): Generates descriptive statistics (count, mean, std, min, max, etc.).
    df.shape: Returns the dimensions (rows, columns).
    df.columns: Returns the column labels.
    df.index: Returns the index labels.
    df['column'].value_counts(): Counts the occurrences of each unique value in a column.

**Data Selection/Filtering**

    df['column']: Selects a single column.
    df[['col1', 'col2']]: Selects multiple columns.
    df.loc[row_label, col_label]: Selects data by labels.
    df.iloc[row_index, col_index]: Selects data by integer-based indexing.
    df[df['column'] > value]: Filters rows based on a condition.
    df.query('column > value'): Filters rows using a query expression.

**Data Manipulation**

    df['new_column'] = value: Creates a new column or modifies an existing one.
    df.drop('column', axis=1): Drops a column.
    df.dropna(): Drops rows with missing values.
    df.fillna(value): Fills missing values with a specified value.
    df['column'].astype(dtype): Converts a column to a different data type.
    df.rename(columns={'old_name': 'new_name'}): Renames columns.
    df.sort_values('column', ascending=True): Sorts DataFrame by a column.
    df.groupby('column').agg({'col2': 'sum', 'col3': 'mean'}): Groups data by a column and applies aggregation functions.
    df.apply(function): Applies a function along an axis.
    df.merge(df2, on='key', how='inner'): Merges two DataFrames based on a common column.
    df.pivot(index='index_col', columns='col_col', values='value_col'): Reshapes a DataFrame using pivot.
    pd.melt(df, id_vars=['id_col'], value_vars=['col1', 'col2']): Unpivots a DataFrame from wide to long format. 

**Handling Missing Data**

    df.isnull(): Checks for missing values (returns boolean mask).
    df.notnull(): Checks for non-missing values (returns boolean mask).
    df.dropna(): Drops rows with any missing values.
    df.dropna(axis=1): Drops columns with any missing values.
    df.fillna(value): Fills all missing values with the specified value.
    df['column'].fillna(df['column'].mean()): Fills missing values with the mean of the column. 

**Other Operations**

    df.duplicated(): Detects duplicate rows.
    df.drop_duplicates(): Removes duplicate rows.
    df.sample(n): Selects a random sample of rows.
    df.set_index('column'): Sets a column as the index.
    df.reset_index(): Resets the index.


