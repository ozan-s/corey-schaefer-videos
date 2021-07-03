# Python Pandas Tutorial (Part 5): Updating Rows and Columns - Modifying Data Within DataFrames
[Video](https://www.youtube.com/watch?v=DCDe29sIKcE)

## Rename all columns at once
    df.columns = ['last_name', 'first_name', 'email']

## Make all column names uppercase
    df.columns = [x.upper() for x in df.columns]
    
## Replace spaces in the column names with _
    df.columns = df.columns.str.replace(' ', '_')
    
## Rename columns using a dictionary
    df.rename(columns={'first_name': 'first', 'last_name': 'last'}, inplace=True)
    
## Change an entire row
    df.loc[2] = ['John', 'Smith', 'JohnSmith@email.com']

## Change specific values in a row
    df.loc[2, ['last', 'email']] = ['Doe', 'JohnDoe@email.com']

## Change single value
    df.loc[2, 'last'] = 'Smith'
    df.at[2, 'last'] = 'Doe'
    
## Change values using a filter
    filt = (df['email'] == 'JohnDoe@email.com')
    df.loc[filt, 'last'] = 'Smith'
    
## Change all values in a single column
    df['email'] = df['email'].str.lower()

## Apply a function to a series
    df['email'].apply(len)
    
    def update_email(email):
        return email.upper()
    df['email'] = df['email'].apply(update_email)
    
    df['email'] = df['email'].apply(lambda x: x.lower())

## Apply a function to a dataframe (to columns by default)
    df['email'].apply(len)

### Apply a function to rows of a dataframe
    df.apply(len, axis='columns')

## Find minimum value of each column using `apply`
    df.apply(pd.Series.min)
    df.apply(lambda x: x.min())

## Apply a function to all values in a dataframe
    df.applymap(len)
    df.applymap(str.lower)

## Substitute each value in a series
    df['first'].map({'Corey': 'Chris', 'Jane': 'Mary'})
### Values not included in the dictionary will be NaN

## Replace values in a series
    df['first'] = df['first'].replace({'Corey': 'Chris', 'Jane': 'Mary'})
### Values not included in the dictionary do not change
    
