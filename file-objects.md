# Python Tutorial: File Objects - Reading and Writing to Files
[Video](https://www.youtube.com/watch?v=Uh2ebFW8OYM)

## Open a file in different modes
    f = open("test.txt", "r") # read
    f = open("test.txt", "w") # write
    f = open("test.txt", "a") # append
    f = open("test.txt", "r+") # read and write
    f.name # get filename
    f.mode # get mode file is open
    f.close() # close the file
    
### Need to explicitly close the file if this method is used

## Open file using context manager
    with open("test.txt", "r") as f:
	    pass
        
## Read the contents of a file
### Small Files: Load all lines in a string
    f_contents = f.read()

### Big Files: Load each line as an item in the list
	f_contents = f.readlines()
    
    f_contents = f.readline() # read line by line, like an iterator
   
	for line in f: # Iterating through the file
        print(line, end = '') # print without a new line break

## Read only part of the file
    f_contents = f.read(100) # read first 100 charachters
    f_contents = f.read(100) # read next 100 charachters
    
## Iterating through small chunks:
    size_to_read = 100
	f_contents = f.read(size_to_read)
	while len(f_contents) > 0:
        print(f_contents)
		f_contents = f.read(size_to_read)    

    f.tell() # Get the position in the file
    f.seek(0) # Go to beginning of the file
    
## Writing to files
    with open("test2.txt", "w") as f: # overwrites file if exists
        f.write("Test") # Test
	    f.write("Test") #TestTest
	    f.seek(0) # go to the beginning
        f.seek("R") # RestTest     
        
## Copying Files:
    with open("test.txt", "r") as rf:
	    with open("test_copy.txt", "w") as wf:
		    for line in rf:
			    wf.write(line)

## Copying image:
    with open("bronx.jpg", "rb") as rf: # need to open in binary read mode
	    with open("bronx_copy.jpg", "wb") as wf: # need to open in binary write mode
		    for line in rf:
			    wf.write(line)

## Copying the image with chunks:
    with open("bronx.jpg", "rb") as rf:
	    with open("bronx_copy.jpg", "wb") as wf:
		    chunk_size = 4096
        rf_chunk = rf.read(chunk_size)
        while len(rf_chunk) > 0:
            wf.write(rf_chunk)
            rf_chunk = rf.read(chunk_size)
