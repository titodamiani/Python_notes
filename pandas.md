# Pandas notes

### Commands

#### Index cell within df
Given a dataframe `df_name`, the column `column_name` and the row index `idx` of interest:
`df_name.iloc[idx]['column_name']` or `df_name['column_name'].iloc[idx]`


Count non-NA values in a series = Series.count()
Count unique values in series = Series.value_counts()
