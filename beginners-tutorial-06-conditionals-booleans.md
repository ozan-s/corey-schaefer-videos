# Python Tutorial for Beginners 6: Conditionals and Booleans - If, Else, and Elif Statements
[Video](https://www.youtube.com/watch?v=DZwmZ8Usvnk)

## Simple conditional
    if True:
        print('Conditional was True')
        
    if False:
        print('Conditional was True')
    
    language = 'Python'
    if language == 'Python':
        print('Conditional was True')
        
## Comparisons:
### Equal:            
    ==
### Not Equal:        
    !=
### Greater Than:     
    >
### Less Than:        
    <
### Greater or Equal: 
    >=
### Less or Equal:    
    <=
### Object Identity:  
    is
 
## Conditional with else statement
    language = 'Python'
    if language == 'Python':
        print('Language is Python')
    else:
        print('No match')
        
## Multiple conditionals
    language = 'Python'
    if language == 'Python':
        print('Language is Python')
    elif language == 'Java':
        print('Language is Java')
    else:
        print('No match')
        
## Boolean operators
### And
    and
### Or
    or
### Not
    not
    
## Conditional with boolean operator
    user = 'Admin'
    logged_in = True
    if user == 'Admin' and logged_in:
        print('Admin page')
    else:
        print('Bad Creds')
    
    if not logged_in:
        print('Please Log In')
    else:
        print('Welcome')
        
## Check for equality of object identity
    a = [1, 2, 3]
    b = [1, 2, 3]
    print(a == b) # True
    print(a is b) # False
    
    a = [1, 2, 3]
    b = a
    print(a == b) # True
    print(a is b) # True
    
## Values evaluated as False
### False
    False
### None
    None
### Zero of any numeric type
    0
    0.0
### Any empty sequence. For example, '', (), [].
    ''
    ()
    []
### Any empty mapping. For example, {}.
    {}
