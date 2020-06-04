# Reading Notes 19  

## Articles  

### Python Regular Expressions Tutorial  
* [Link to Article](https://www.datacamp.com/community/tutorials/python-regular-expression-tutorial)  
Regular expressions are supported by the `re` module. This means in order to use them within your python scripts you must import them.:  
- `import __` or `import re`

Basic Patterns: Ordinary Characters  
```py
import re

pattern = r'Cookie' # r in front is a raw string literal. Such literals are stored as they appear.
sequence = 'Cookie'

if re.match(pattern, sequence):
    print('Match!')
else:
    print('Not a match!')
```

`match()`: checks for a match only at the beginning of the strong(by default).  
`search()`: checks for a match anywhere in the string.  

`findAll(pattern, string, flags=0)`:
```py
email_address = "Please contact us at: support@datacamp.com, xyz@datacamp.com"

#'addresses' is a list that stores all the possible match
addresses = re.findall(r'[\w\.-]+@[\w\.-]+', email_address)
for address in addresses: 
    print(address)
```

Regex is used in a lot of pre-processing of data and it is an important skill to know how to use.


### Shutil  
* [Link to Article](https://pymotw.com/3/shutil/)  
shutil is a module with a purpose of: high-level file operations.  
- Copying Files:  
    - `copyfile()` copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.  
- Copying File MetaData:  
    - `copymode()`: To copy the permissions from one file to another.  
- Working with Directory Trees  
    - shutil includes three functions to work with trees:  
        - `copytree()`: To copy a directory from one place to another.  
        - `rmtree()`: To remove a directory and its contents.  
        - `move()`: To move a file or directory from one place to another.  
- Finding Files:  
    - `which()`: Scans a search path looking for a file name.  
- Archives:  
    - `make_archive()`: Creates a new archive file.  
    - `unpack_archive()`: Extract an archive.  
- File System Space:  
    - `disk_usage()`: Examines the local file system to see how much space is available before performing a long running operation that may exhaust that space, returns a tuple with the total space.  
    
## Additional Resources  
### Videos  
* [Automation Ideas](https://www.youtube.com/watch?v=qbW6FRbaSl0&t=69s)  
* [Automating Your Browser and Desktop Apps](https://www.youtube.com/watch?v=dZLyfbSQPXI)  

## Bookmark/Skim  
* [Watchdog](https://pythonhosted.org/watchdog/)  

