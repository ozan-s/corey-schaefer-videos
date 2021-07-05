# Python Pandas Tutorial (Part 9): Cleaning Data - Casting Datatypes and Handling Missing Values
[Video](https://www.youtube.com/watch?v=KdmPHEnPJPs)

## Dataframe used in the video
    people = {
    'first': ['Corey', 'Jane', 'John', 'Chris', np.nan, None, 'NA'], 
    'last': ['Schafer', 'Doe', 'Doe', 'Schafer', np.nan, np.nan, 'Missing'], 
    'email': ['CoreyMSchafer@gmail.com', 'JaneDoe@email.com', 'JohnDoe@email.com', None, np.nan, 'Anonymous@email.com', 'NA'],
    'age': ['33', '55', '63', '36', None, None, 'Missing']
    }

## Drop rows with NaN values
    df.dropna()
    df.dropna(axis='index', how='any')
    
## Drop rows with NaN values only on certain columns
    df.dropna(axis='index', how='any', subset=['email'])
    df.dropna(axis='index', how='all', subset=['last', 'email'])
    
## Replace custom missing values with NaN
    df.replace('NA', np.nan, inplace=True)
    df.replace('Missing', np.nan, inplace=True)
    
## Get a mask of NaN values
    df.isna()

## Replace NaN values with a custom value
    df.fillna('MISSING')
    
## Get a list of data types in the dataframe
    df.dtypes

## Convert column to integer
    df['age'] = df['age'].astype(int)
   
### This will generate an error if NaN is in the column. NaN is actually a float.

## Convert column to float and do analysis
    df['age'] = df['age'].astype(float)   
    df['age'].mean()

## Replace custom missing values with NaN during dataframe creation
    na_vals = ['NA', 'Missing']
    df = pd.read_csv('data/survey_results_public.csv', index_col='Respondent', na_values=na_vals)
    
## Find out the unique values in a column
    df['YearsCode'].unique()

## Cleanup text only data, convert to float and do analysis
    df['YearsCode'].replace('Less than 1 year', 0, inplace=True)
    df['YearsCode'].replace('More than 50 years', 51, inplace=True)
    df['YearsCode'] = df['YearsCode'].astype(float)
    df['YearsCode'].mean()
    df['YearsCode'].median()

