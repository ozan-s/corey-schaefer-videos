## Python Tutorial: OS Module - Use Underlying Operating System Functionality
[Video](https://www.youtube.com/watch?v=tJxcKyFMTGo)

## Import the os module
    import os

## See all attributes and methods of a module
    print(dir(os))

## Get current working directory
    os.getcwd()

## Change directory
    os.chdir('Users/coreyschaefer/Desktop') 

## List contents of a directory
    os.listdir()
    os.listdir(path)

## Create directories
    os.mkdir('OS-Demo-2')  # Create single directory
    os.makedirs('OS-Demo-2/Sub-Dir-1') # Creates top level directory if it doesn't exists 

## Remove directories
    os.rmdir('OS-Demo-2/Sub-Dir-1'). # Remove single
    os.removedirs('OS-Demo-2/Sub-Dir-1')  # Removes intermediate directories if specified

## Rename a file or folder
    os.rename(‘test.txt’, ‘demo.txt’). # This renames text.txt to demo.txt

## Look at info about files
    os.stat(test.txt)

### Useful stat results: st_size (bytes), st_mtime (time stamp)
    mod_time = os.stat('demo.txt'.st_mtime
    datetime.fromtimestamp(mod_time)

## To see entire directory tree and files within
    os.walk('Users/coreyschaefer/Desktop')
    
### os.walk is a generator that yields a tuple of 3 values as it walks the directory tree

    for dirpath, dirnames, filenames in os.walk(routepath): 
        print(‘Current Path:’, dirpath)
        print(‘Directories:’, dirnames)
        print(‘Files:’, filenames)
        print()

## Access environment variable
    os.environ.get(‘HOME’)

## Create a file path
    file_path = os.path.join(os.environ.get(‘HOME’), ‘test.txt’)

## Get filename of any path we are working on
    os.path.basename(‘/tmp/test.txt’) # test.txt

## Get directory name of any path we are working on
    os.path.dirname(‘/tmp/test.txt’) # /tmp

## Get directory and file names as a tuple
    os.path.split(‘/tmp/test.txt’) # ('/tmp', 'test.txt')

## Check if the path exists
    os.path.exists(‘/tmp/test.txt’) # True

## Check if it is a directory
    os.path.isdir(‘/tmp/test.txt’) # False

## Check if it is a file
    os.path.isfile(‘/tmp/test.txt’) # True

## Split the route and file extension
    os.path.splitext(‘/tmp/test.txt’) # (‘/tmp/test’, ‘.txt’)
