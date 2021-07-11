# Python Tutorial for Beginners 9: Import Modules and Exploring The Standard Library
[Video](https://www.youtube.com/watch?v=CqvZ3vGoGs0)

## Import a user made module in the same directory as the main file
    import my_module
    
### When a module is imported, all code on the module is run

## Use a function in the imported module
    my_module.find_index()
    
## Import module with a alias
    import my_module as mm
    mm.find_index()
    
## Import only the function from the module
    from my_module import find_index
    find_index()
    
## Import multiple items from a module
    from my_module import find_index, test
    find_index()
    test
    
    from my_module import find_index as fi, test
    fi() # not recommended as it reduces readability
    test
    
## Import everything from a module
    from my_module import * # not recommended as it makes debugging difficult

## See which paths are checked when importing modules
    import sys
    sys.path
    
## Add a new directory to the path
    sys.path.append('/Users/coreyschaefer/Desktop/My-Modules')
    
### Better way is to add the path to the PYTHONPATH environment variable on your machine

## Import modules from the standard library
    import random
    random_course = random.choice(courses)
    
## Other useful standard libaries
    import math
    import datetime
    import calendar
    import os
    
## Find the location of a module file
    os.__file__
