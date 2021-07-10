# Python Tutorial: Sorting Lists, Tuples, and Objects
[Video](https://www.youtube.com/watch?v=D3JvDWO-BY4)

    li = [9, 1, 8, 2, 7, 3, 6, 4, 5]
    
## Sort using sorted() function
    s_li = sorted(li) # Original list remains unsorted
    
## Sort using sort() method
    li.sort() # Original list is sorted
    
## Sort in reverse order
    s_li =  sorted(li, reverse=True)
    li.sort(reverse=True)
    
## Sort a tuple
    tup = (9, 1, 8, 2, 7, 3, 6, 4, 5)
    s_tup = sorted(tup) # Returns a sorted list
    
## Sort a dictionary
    s_dict = sorted(dict) # Returns a list of sorted keys
    
## Sort a list by absolute values
    s_li = sorted(li, key=abs) 

### Sorts list by running each element through abs() function first before making a comparison

## Sort objects using attributes
### By defining a custom function    
    def e_sort(emp):
        return emp.name
        
    s_employees = sorted(employees, key=e_sort)

### By defining a lambda function
    s_employees = sorted(employees, key=lambda e: e.name)
    
### By using attrgetter function
    from operator import attrgetter
    s_employees = sorted(employees, key=attrgetter('name'))    
