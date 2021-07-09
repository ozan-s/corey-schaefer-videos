# Python Tutorial for Beginners 8: Functions
[Video](https://www.youtube.com/watch?v=9Os0o3wzS_I)

## Create a placeholder function
    def hello_func():
        pass
  
    hello_func()
    
## Create a function    
    def hello_func():
        print('Hello Function!')
        
    hello_func()
    
## Create a function that returns a value
    def hello_func():
        return 'Hello Function.'
        
    print(hello_func()) # Returns a string
    print(hello_func().upper()) # Use string method on the return value
    
## Passing arguments to a function
    def hello_func(greeting):
        return '{} Function.'.format(greeting)
        
    print(hello_func('Hi'))
    
## Setting defaults for arguments
    def hello_func(greeting, name='You'):
        return '{}, {}.'.format(greeting, name)
        
    print(hello_func('Hi'))
    print(hello_func('Hi', name='Corey'))
    
## Creating function with multiple arguments and keyword arguments
    def student_info(*args, **kwargs):
        print(args)
        print(kwargs)
        
    student_info('Math', 'Art', name='John', age=22)
### args will be a tuple and kwargs will be a dictionary

## To pass a tuple and a dictionary as arguments to a function, use * and ** to unpack them inside the function
    courses = ['Math', 'Art']
    info = {'name':'John', 'age':22}
    student_info(*courses, **info)

## Example function
    # Number of days per month. First value placeholder for indexing purposes.
    month_days = [0, 31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]


    def is_leap(year):
        """Return True for leap years, False for non-leap years."""

        return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)


    def days_in_month(year, month):
        """Return number of days in that month in that year."""

        # year 2017
        # month 2
        if not 1 <= month <= 12:
            return 'Invalid Month'

        if month == 2 and is_leap(year):
            return 29

        return month_days[month]

    print(days_in_month(2017, 2))
        
