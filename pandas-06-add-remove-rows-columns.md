# Python Pandas Tutorial (Part 6): Add/Remove Rows and Columns From DataFrames
[Video](https://www.youtube.com/watch?v=HQ6XO9eT-fc)

## Create new column based on other columns
    df['full_name'] = df['first'] + ' ' + df['last']

## Delete existing columns
    df.drop(columns=['first', 'last'], inplace=True)

## Split existing column into two columns
    df[['first', 'last']] = df['full_name'].str.split(' ', expand=True)
 
## Add a new row to the dataframe
    df.append({'first': 'Tony'}, ignore_index=True)

## Add one dataframe to another
    df.append(df2, ignore_index=True, sort=False)

## Remove single row from the dataframe
    df.drop(index=4)

## Remove rows fitting a criteria
    df.drop(index=df[df['last'] == 'Doe'].index)
    
    filt = df['last'] == 'Doe'
    df.drop(index=df[filt].index)
