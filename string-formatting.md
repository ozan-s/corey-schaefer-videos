# Python Tutorial: String Formatting - Advanced Operations for Dicts, Lists, Numbers, and Dates
[Video](https://www.youtube.com/watch?v=vTX3IwquFkc)

    person = {'name': 'Jenn', 'age': 23}

## Using string concatenation 
    sentence = 'My name is ' + person['name'] + ' and I am ' + str(person['age']) + ' years old.'
 
## Using format method
    sentence = 'My name is {} and I am {} years old.'.format(person['name'], person['age'])

    sentence = 'My name is {0} and I am {1} years old.'.format(person['name'], person['age'])
    
## Repeating string
    tag = 'h1'
    text = 'This is a headline'

    sentence = '<{0}>{1}</{0}>'.format(tag, text)
    
## Using dictionary in the format
    sentence = 'My name is {0['name']} and I am {0['age']} years old.'.format(person)
    
## Using class attributes
    sentence = 'My name is {0.name} and I am {0.age} years old.'.format(p1)

## Using keyword arguments
    sentence = 'My name is {name} and I am {age} years old.'.format(name='Jenn', age='30')
    
    person = {'name': 'Jenn', 'age': 23}
    sentence = 'My name is {name} and I am {age} years old.'.format(**person)

## Format numbers
    for i in range(1, 11):
        sentence = 'The value is {}'.format(i) # 1, 2, 3, ...
        sentence = 'The value is {:02}'.format(i) # 01, 02, 03, ...

    pi = 3.14159265
    sentence = 'Pi is equal to {:.2f}'.format(pi) # 3.14
    
    sentence = '1 MB is equal to {:,} bytes'.format(1000**2) # 1,000,000
    sentence = '1 MB is equal to {:,.2f} bytes'.format(1000**2) # 1,000,000.00
    
## Format dates
    import datetime
    my_date = datetime.datetime(2016, 9, 24, 12, 30, 45)
    
    sentence = '{:%B %d, %Y}'.format(my_date) # March 01, 2016
    
    sentence = '{0:%B %d, %Y} fell on a {0:%A} and was the {0:%j} day of the year'.format(my_date)
    # March 01, 2016 fell on a Tuesday and was the 061 day of the year.        
