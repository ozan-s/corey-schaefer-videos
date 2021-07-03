# Python Pandas Tutorial (Part 3): Indexes - How to Set, Reset, and Use Indexes
[Video](https://www.youtube.com/watch?v=W9XjRYFkkyw)

## Change index of a dataframe permanently
    df.set_index('email', inplace=True)

## Display index of a dataframe
    df.index

## Access data on a row using labels
    df.loc['CoreyMSchafer@gmail.com']
    df.loc['CoreyMSchafer@gmail.com', 'last']
    
## Reset index
    df.reset_index(inplace=True)
    
## Set index while importing data into a dataframe
    df = pd.read_csv('data_file_to_import.csv', index_col='Respondent')
    
## Sort indexes
    df.sort_index()
    df.sort_index(ascending=False)
