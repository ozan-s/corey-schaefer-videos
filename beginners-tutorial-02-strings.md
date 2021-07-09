# Python Tutorial for Beginners 2: Strings - Working with Textual Data
[Video](https://www.youtube.com/watch?v=k9TUPpGqYTo)
## Escape a character in a string
    message = 'Bobby\'s World'
## Multi-line string
    message = """Bobby's World was a goodcartoon in the 1990s"""
## Length of string
    len(message)
## First character in a string
    message[0]
## First five characters in a string - slicing
    message[0:5]
    message[:5]
## String formatting
    message = '{}, {}. Welcome!'.format(greeting, name)
## f string
    message = f'{greeting}, {name.upper(). Welcome!}'
## Atrributes and methods of a variable
    print(dir(message))
## Help function - use on a class, not variable
    print(help(str))
    print(help(str.lower))
