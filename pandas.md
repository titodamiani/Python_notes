# Pandas notes

### Commands

#### Index cell within df
Given a dataframe `df_name`, the column `column_name` and the `index` of interest:
`df_name.iloc[1]['column_name']` or `df_name['column_name'].iloc[1]`