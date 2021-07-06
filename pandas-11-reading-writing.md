# Python Pandas Tutorial (Part 11): Reading/Writing Data to Different Sources - Excel, JSON, SQL, Etc
[Video](https://www.youtube.com/watch?v=N6hyN6BW6ao)

## Read from CSV
    df = pd.read_csv('data/survey_results_public.csv', index_col='Respondent')
    schema_df = pd.read_csv('data/survey_results_schema.csv', index_col='Column')
    
## Write to CSV
    filt = (df['Country'] == 'India')
    india_df = df.loc[filt]
    india_df.to_csv('data/modified.csv')

## Write to CSV tab demilited
    india_df.to_csv('data/modified.tsv', sep='\t')

## Write and read XLS
    india_df.to_excel('data/modified.xlsx')
    test = pd.read_excel('data/modified.xlsx', index_col='Respondent')

## Read and write JSON
    india_df.to_json('data/modified.json', orient='records', lines=True)
    test = pd.read_json('data/modified.json', orient='records', lines=True)

## Read and write database
    from sqlalchemy import create_engine
    import psycopg2
    engine = create_engine('postgresql://dbuser:dbpass@localhost:5432/sample_db')
    india_df.to_sql('sample_table', engine, if_exists='replace')
    sql_df = pd.read_sql('sample_table', engine, index_col='Respondent')
    sql_df = pd.read_sql_query('SELECT * FROM sample_table', engine, index_col='Respondent')

## Read JSON from internet
    posts_df = pd.read_json('https://raw.githubusercontent.com/CoreyMSchafer/code_snippets/master/Python/Flask_Blog/snippets/posts.json')
