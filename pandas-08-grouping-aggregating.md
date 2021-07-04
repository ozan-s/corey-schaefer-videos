# Python Pandas Tutorial (Part 8): Grouping and Aggregating - Analyzing and Exploring Your Data
[Video](https://www.youtube.com/watch?v=txMdrV1Ut64)

## Display first 15 values in a series
    df['ConvertedComp'].head(15)

## Calculate median of a series
    df['ConvertedComp'].median()

## Calculate median of all possible series 
    df.median()
    
## Do a quick statistical analysis of all series
    df.describe()
    
## Count the number of non NaN values in a series
    df['ConvertedComp'].count()

## Breakdown of values in a series
    df['SocialMedia'].value_counts()
    df['SocialMedia'].value_counts(normalize=True)

## Group data
    country_grp = df.groupby(['Country'])
    country_grp.get_group('India')

## Run aggregate function on the whole group
    country_grp['SocialMedia'].value_counts()

## Run aggregate function on part of the group using index
    country_grp['SocialMedia'].value_counts(normalize=True).loc['China']
    country_grp['ConvertedComp'].median().loc['Germany']

## Run multiple aggregate functions
    country_grp['ConvertedComp'].agg(['median', 'mean']).loc['Canada']

## Using filters and groupby to get same result
    filt = df['Country'] == 'India'
    df.loc[filt]['LanguageWorkedWith'].str.contains('Python').sum()
    
    country_grp['LanguageWorkedWith'].apply(lambda x: x.str.contains('Python').sum())

## Concatenate two series into one dataframe
    country_respondents = df['Country'].value_counts()
    country_uses_python = country_grp['LanguageWorkedWith'].apply(lambda x: x.str.contains('Python').sum())
    python_df = pd.concat([country_respondents, country_uses_python], axis='columns', sort=False)

## Add a new column based on the other two columns
    python_df.rename(columns={'Country': 'NumRespondents', 'LanguageWorkedWith': 'NumKnowsPython'}, inplace=True)
    python_df['PctKnowsPython'] = (python_df['NumKnowsPython']/python_df['NumRespondents']) * 100
    python_df.sort_values(by='PctKnowsPython', ascending=False, inplace=True)


    
