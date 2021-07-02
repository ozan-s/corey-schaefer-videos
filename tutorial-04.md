# Python Tutorial for Beginners 4: Lists, Tuples, and Sets
[Video](https://www.youtube.com/watch?v=W8KRzm-HUcc)

## Create a list
    courses = ['History', 'Math', 'Physics', 'CompSci']

## Add item to a list
    courses.append('Art')

## Add item to a specific location
    courses.insert(0, 'Art')

## Add items to a list individually from another list
    courses.extend(courses_2)

## Remove item from a list
    courses.remove('Math')

## Pop-out last item in a list
    popped = course.pop()

## Reverse a list
    courses.reverse()

## Sort a list
    courses.sort()
    courses.sort(reverse=True)
    sorted_courses = sorted(courses)

## Get min, max, sum
    min(nums)
    max(nums)
    sum(nums)

## Find location of an item in a list
    courses.index('CompSci')

## Check item is in a list
    'Art' in courses

## Enumerate through a list, starting from 1
    for index, course in enumerate(courses, start=1):
        print(index, courses)

## Create string from a list, separated by commas
    course_str = ', '.join(courses)

## Split a string into a list
    new_list = course_str.split

## Create a tuple (cannot be changed)
    courses = ('History', 'Math', 'Physics', 'CompSci')

## Create a set (unsorted, no duplicates allowed)
    cs_courses = {'History', 'Math', 'Physics', 'CompSci'}

## Find intersection of two sets
    cs_courses.intersection(art_courses)

## Find difference between two sets
    cs_courses.difference(art_courses)

## Combine two sets
    cs_courses.union(art_courses)

## Create empty list
    empty_list = []
    empty_list = list()

## Create empty tuple
    empty_tuple = ()
    empty_tuple = tuple()

## Create empty set
    empty_set = set()
