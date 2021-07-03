# Python Pandas Tutorial (Part 4): Filtering - Using Conditionals to Filter Rows and Columns
[Video](https://www.youtube.com/watch?v=Lw2rlcxScZY)

## Create a filter mask
    filt = (df['last'] == 'Doe')
    
### `filter` is an assigned name, so don't use it!
### Paranthesis is not needed, but good practice to have thme. 

## Apply filter mask to the dataframe
    df[filt]
    df[df['last'] == 'Doe']
    df.loc[filt]
    df.loc[filt, 'email']
    
## Using logic operators: & AND | OR
    filt = (df['last'] == 'Doe') & (df['first'] == 'John')
    filt = (df['last'] == 'Schafer') | (df['first'] == 'John')
    
## Finding items that don't match the criters
    df.loc[~filt, 'email']
    
## Filtering examples
    high_salary = (df['ConvertedComp'] > 70000)
    df.loc[high_salary, ['Country', 'LanguageWorkedWith', 'ConvertedComp']]
    
    countries = ['United States', 'India', 'United Kingdom', 'Germany', 'Canada']
    filt = df['Country'].isin(countries)
    df.loc[filt, 'Country']
    
    filt = df['LanguagesWorkedWith].str.contains('Python', na=False)
