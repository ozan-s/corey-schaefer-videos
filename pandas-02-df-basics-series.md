# Python Pandas Tutorial (Part 2): DataFrame and Series Basics - Selecting Rows and Columns
[Video](https://www.youtube.com/watch?v=zmdjNSmRXF4&list=PL-osiE80TeTsWmV9i9c58mdDCSskIFdDS)

## Create dataframe from dictionary
    people = {
    "first": ["Corey", 'Jane', 'John'], 
    "last": ["Schafer", 'Doe', 'Doe'], 
    "email": ["CoreyMSchafer@gmail.com", 'JaneDoe@email.com', 'JohnDoe@email.com']
    }
    
    df = pd.DataFrame(people)
    
## Access values of a single column, returns a Series object
    df['email']
    df.email
### Dataframe is a container for multiple Series objects

## Access values of multiple columns, returns a Dataframe object
    df[['last', 'email']]
    
## Get a list of columns in the dataframe
    df.columns
    
## Access values on specific rows using integer location
    df.iloc[0]
    df.iloc[[0, 1]]
    
## Access values on specific rows and column using integer location
    df.iloc[[0, 1], 2]
    
## Access values on specific rows using labels
    df.loc[0]
    
## Access values on specific rows and column using labels
    df.loc[[0, 1], ['email', 'last']]
    
## Get the value count of a Series
    df.['Hobbyist'].value_counts()
    
## Use slicing to access multiple rows and columns
    df.loc[0:2, 'Hobbyist']
    df.loc[0:2, 'Hobbyist':'Employment']
### The last value is included in the slice!
