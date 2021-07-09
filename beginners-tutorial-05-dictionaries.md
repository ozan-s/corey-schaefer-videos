# Python Tutorial for Beginners 5: Dictionaries - Working with Key-Value Pairs
[Video](https://www.youtube.com/watch?v=daefaLgNkw0)

## Create dictionary {key: value}
    student = {'name': 'John', 'age': 25, 'courses': ['Math', 'CompSci']}

## Access to value of one key
    student['name']
### Returns a KeyError if key doesn't exists.
    
## Access to value of one key
    student.get('phone')
### Returns None if key doesn't exists
    
    student.get('phone', 'Not Found')
### Returns string if key doesn't exists

## Set a new key
    student['phone'] = '555-5555'

    student['name'] = 'Jane'
### Updates the key if it exists

## Update multiple keys
    student.update({'name': 'Jane', 'age': 26, 'phone':'555-5555'})
    
## Delete single key.
    del student['age']
    
## Remove key from dictionary and assign it to a variable
    age = student.pop('age')
    
## Get the number of keys in a dictionary
    len(student)
    
## Get a list of all keys
    student.keys()
    student.values()
    student.items()
    
## Loop through the keys and values
    for key, value in student.items():
        print(key, value)
    
