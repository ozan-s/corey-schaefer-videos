# Python Pandas Tutorial (Part 7): Sorting Data
[Video](https://www.youtube.com/watch?v=T11QYVfZoD0)

## Sort by values in one column
    df.sort_values(by='last', ascending=True)
    
## Sort by values in more than one column
    df.sort_values(by=['last', 'first'], ascending=True)
    df.sort_values(by=['last', 'first'], ascending=[False, True], inplace=True)

## Sort by index
    df.sort_index()

## Sort single column
    df['last'].sort_values()

## Sort by multiple columns
    df.sort_values(by=['Country', 'ConvertedComp'], ascending=[True, False], inplace=True)
    
## Find 10 largest values in a series
    df['ConvertedComp'].nlargest(10)
        
    df.nlargest(10, 'ConvertedComp')

