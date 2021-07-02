# Python Pandas Tutorial (Part 1): Getting Started with Data Analysis - Installation and Loading Data
[Video](https://www.youtube.com/watch?v=ZyhVh-qRZPA&t=626s)

## Install pandas and Jupyter
    pip install pandas
    pip install jupyterlab
    
## Start Jupyter Notebook
    jupyter notebook

## Import pandas, load file into a dataframe and print
    import pandas as pd
    df = pd.read_csv('data_file_to_import.csv')
    df
    
## Get number of rows and columns of a dataframe
    df.shape
    
## Get detailed information about the columns
    df.info()
 
 ## Set maximum columns and rows to display to 99
    pd.set_option('display.max_columns', 99)
    pd.set_option('display.max_rows', 99)
    
## Display first and last rows of the dataframe
    df.head()
    df.tail()
    df.head(10)
    df.tail(10)
    
