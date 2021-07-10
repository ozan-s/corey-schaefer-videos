# Python Tutorial: Comprehensions - How they work and why you should be using them
[Video](https://www.youtube.com/watch?v=3dt4OGnU5sM)

    nums = [1,2,3,4,5,6,7,8,9,10]

## Simple list comprehension to replace a for loop

    my_list = []
    for n in nums:
      my_list.append(n)
    print(my_list)

    print([n for n in nums]) # List comprehension
    
    my_list = []
    for n in nums:
        my_list.append(n*n)
    print(my_list)
    
    print([n*n for n in nums]) # List comprehension
    
    # Using a map + lambda, but less readable
    my_list = map(lambda n: n*n, nums)
    print(list(my_list))
    
## List comprehension with if statement
    # I want 'n' for each 'n' in nums if 'n' is even
    my_list = []
    for n in nums:
        if n%2 == 0:
        my_list.append(n)
    print(my_list)
    
    my_list = [n for n in nums in n%2 == 0] # List comprehension
    
    # Using a filter + lambda but less readable
    my_list = filter(lambda n: n%2 == 0, nums)
    print(list(my_list))
    
 ## List comprehension with two variables
    # I want a (letter, num) pair for each letter in 'abcd' and each number in '0123'
    my_list = []
    for letter in 'abcd':
        for num in range(4):
            my_list.append((letter,num))
    print(my_list)
    
    my_list = [(letter, num) for letter in 'abcd' for num in range(4)]

## Dictionary comprehensions
    names = ['Bruce', 'Clark', 'Peter', 'Logan', 'Wade']
    heros = ['Batman', 'Superman', 'Spiderman', 'Wolverine', 'Deadpool']
    print(list(zip(names, heros)))
    
    # I want a dict{'name': 'hero'} for each name,hero in zip(names, heros)
    my_dict = {}
    for name, hero in zip(names, heros):
        my_dict[name] = hero
    print(my_dict)
    
    my_dict = {name:hero for name, hero in zip(names,heroes)} # Dictionary comprehension
    
    my_dict = {name:hero for name, hero in zip (names,heroes) if name != 'Peter'}
    
## Set comprehensions
    nums = [1,1,2,1,3,4,3,4,5,5,6,7,8,7,9,9]
    my_set = set()
    for n in nums:
        my_set.add(n)
    print(my_set)
    
    my_set = {n for n in nums}
    
# Generator expressions
    # I want to yield 'n*n' for each 'n' in nums
    nums = [1,2,3,4,5,6,7,8,9,10]

    def gen_func(nums):
        for n in nums:
            yield n*n

    my_gen = gen_func(nums)

    for i in my_gen:
        print(i)
        
    my_gen = (n*n for n in nums) # Generator expression
