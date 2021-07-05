# Python Pandas Tutorial (Part 10): Working with Dates and Time Series Data
[Video](https://www.youtube.com/watch?v=UFuo7EHI8zc)

# Check if a column is datetime object
    df.loc[0, 'Date'].day_name()

# Convert string to datetime object
    df['Date'] = pd.to_datetime(df['Date'], format='%Y-%m-%d %I-%p')
    
# Convert string to datetime object while loading the data
    d_parser = lambda x: pd.datetime.strptime(x, '%Y-%m-%d %I-%p')
    df = pd.read_csv('ETH_1h.csv', parse_dates=['Date'], date_parser=d_parser)
    
# Run datetime function on entire series
    df['Date'].dt.day_name()
    df['DayOfWeek'] = df['Date'].dt.day_name()

# Do basic calculations with datetime
    df['Date'].min()
    df['Date'].max()
    df['Date'].max() - df['Date'].min()
    
 # Filter datetime data
    filt = (df['Date'] >= '2019') & (df['Date'] <= '2020')
    df.loc[filt]
    
    filt = (df['Date'] >= pd.to_datetime('2019-01-01')) & (df['Date'] < pd.to_datetime('2020-01-01'))
    df.loc[filt]

# Filter datetime using slicing
    df.set_index('Date', inplace=True)
    df['2019']
    df['2020-01':'2020-02']
    df['2020-01':'2020-02']['Close'].mean()
    df['2020-01-01']['High'].max()

# Resample data (from hourly to daily)
    highs = df['High'].resample('D').max()

# Plot inline
    %matplotlib inline
    highs.plot()

# Resample entire dataframe
    df.resample('W').mean()
    df.resample('W').agg({'Close': 'mean', 'High': 'max', 'Low': 'min', 'Volume': 'sum'})
    

