# Python Tutorial for Beginners 7: Loops and Iterations - For/While Loops
[Video](https://www.youtube.com/watch?v=6iF8Xb7Z3wQ)

## Loop through a list
    nums = [1, 2, 3, 4, 5]
    for num in nums:
        print(num)
        
## Use break to break out of the loop
    for num in nums:
    if num == 3:
        print('Found!')
        break
    print(num) # 1 2 Found!
    
## Use continue to skip to the next iteration
    for num in nums:
    if num == 3:
        print('Found!')
        continue
    print(num) # 1 2 Found! 4 5
    
## Have an inner loop inside a loop
    for num in nums:
        for letter in 'abc'
            print(num, letter)
            
## Run a loop for a number of times
    for i in range(10)
        print(i) # 0, 1, 2 ... 9
        
    for i in range(1, 11)
        print(i) # 1, 2, 3 ... 10
        
## While loops
    x = 0
    while x < 10:
        print(x)
        x += 1
        
    x = 0
    while x < 10:
        if x ==5:
            break
        print(x)
        x += 1
        
 ## Infinite loops
    x = 0
    while True:
        print(x)
        x += 1
        
### User Ctrl+C to exit a inifinte loop
