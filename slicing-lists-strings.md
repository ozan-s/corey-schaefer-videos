# Python Tutorial: Slicing Lists and Strings
[Video](https://www.youtube.com/watch?v=ajrtAuDg3yw)

    my_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    #          0, 1, 2, 3, 4, 5, 6, 7, 8, 9
    #        -10,-9,-8,-7,-6,-5,-4,-3,-2,-1
    
## Access single value in a list using index
    my_list[0] # 0
    my_list[-10] # 0

## Access multiple values in a list using index
    # list[start:end:step]
    my_list[0:6]    # [0, 1, 2, 3, 4, 5]
    my_list[3:8]    # [3, 4, 5, 6, 7]
    my_list[-7:-2]  # [3, 4, 5, 6, 7]
    my_list[1:-2]   # [1, 2, 3, 4, 5, 6, 7]
    my_list[5:]     # [5, 6, 7, 8, 9]
    my_list[:-1]    # [0, 1, 2, 3, 4, 5, 6, 7, 8]
    my_list[:]      # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    
## Use step to skip values
    my_list[2:-1:2]     # [2, 4, 6, 8]
    my_list[-1:2:-1]    # [9, 8, 7, 6, 5, 4, 3]
    my_list[-2:1:2]     # [8, 6, 4, 2]

## Reverse the list
     my_list[::-1]      # [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]

## Slicing strings works the same way
    sample_url = 'http://coreyms.com'

## Reverse the url
    sample_url[::-1]

## Get the top level domain
    sample_url[-4:]

## Print the url without the http://
    sample_url[7:]

## Print the url without the http:// or the top level domain
    sample_url[7:-4]
