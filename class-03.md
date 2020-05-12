# Reading Notes 03
- [Table of Contents](README.md)
## Articles  

### Read and Write Files in Python
* [Link to Article](https://realpython.com/read-write-files-python/)  

1. What is a File?  
    - A file is a contiguous set of bytes used to store data.  
    - Byte files are translated into binary 1 and 0 for easier processing by the computer.  
    - Files have three main parts:  
        - Header  
        - Data  
        - End of File (EOF)  
    - Accessing a file requires a file path. This is a string that represents the location. A path also has three parts:  
        - Folder Path  
        - File Name  
        - Extension  
    - Line endings:  
        - Carriage Return: `CR or \r`  
        - Line Feed: `LF or \n`  
        - `CR + LR or \r\n`  
        - Different outputs can occur between a Windows system and a Unix.  
    - Character Encodings: An encoding is a translation from byte data to human readable characters. Two common encodings are:  
        - `ASCII and UNICODE` Formats.  
        - `ASCII` can only store 128 characters.  
        - `Unicode or UTF-8` can contain 1,114,112 characters.  

2. Opening and Closing a File in Python  
    - To open a file in python we invoke a file with `open()` build-in function. Takes a single argument, a path, and returns a file object.  
    - `file = open("somefile.txt")`  
    - After we open a file we must properly close it. If not we don't know when that will happen and could potentially be harmful. There are two ways to accomplish this:  
        - First: Use a `try-finally` block.  
        - Second: Use the `with` statement.
    - Three different categories of file objects:  
        - Text files  
        - Buffered binary Files  
        - Raw binary files  
    - Files are opened in a type of mode: read, write, binary mode and many more.  
3. Reading and Writing Opened Files  
Once you a file is opened you will want to action it. There are multiple methods that can be called on file objects here are a few:  
    - Reading methods:  
        - `.read(size=-1)` Reads a file based on size bytes.  
        - `readline(size=-1)` Reads at most size number of lines  
        - `readlines()` This reads remaining lines of object and returns them as a list.  
    - Writing methods:  
        - `write(string)` does exactly that.  
        - `writelines(seq)`  
4. Tips and Tricks  
    - `__file__` attribute is a special attribute of modules, similiar to `__name__`. Definition: the pathname of the file from which the module was loaded, if it was loaded from a file.  
    - NOTE: `__file__` returns the path relative to where the initial python scrip was called.  
    - NOTE: `os.getcwd()` will get you the current working directory of your executing code.  
    - Appending to a File:  
        - Sometimes you want to append or add code to the end of an existing file. This can be achieved by using the `a` mode when opeing the file.  
    - You can work in two files at the same time. By combining the methods like this:  
        - `with open(some_path, 'r') as reader, open(some_other_path, 'w') as writer: `  
5. Don't Re-Invent the Snake  
    - There is plenty of documentation out there to deal with many file types in Python. Two common file types you will work with are `.csv` and `.json`. Below are two articles for reference:  
        - [Reading and Writing CSV Files in Python](https://realpython.com/python-csv/)  
        - [Working With JSON Data in Pythong](https://realpython.com/python-json/)  
### Exceptions in Python  
* [Link to Article](https://realpython.com/python-exceptions/)  

1. Exceptions versus Snytax Errors  
Snyax errors occur when the parser detects an incorrect statement. An exception error occurs when syntactically correct Python code results in an error.

2. Raising an Exception: We can use `raise` to throw an exception if a condition occurs.  
    - This statment can be a custom exception.  
    - `raise Exception('Do not exceed the value')`  
        - Allows you to thrown an exception at any time.  

3. The AssertionError Exception: Instead of waiting for a program crash you can make an assertion.  
    - `assert` that a condition is met. If false an assertion error is thrown.  
        - Enables you to verify if a certain condition is met and thrown an exception if it isn't.  

4. The try and except Block: Handling Exceptions: Used to catch and handle exceptions.
    - `try` is normal code you want to run.  
        - All statments are exceuted until an exception is encountered.  
    - `except` follows try and will handle exceptions if errors occur or conditions are not met. 
        - Used to catch and handle exception(s) that are encountered in the try clause.  

5. The else Clause: This is statment can run certain block oif code in the absence of exceptions.  
    - `try` Run this code.  
    - `except` Execute this code when there is an exception  
    - `else` No exceptions? Run this code  
        - lets you code sections that should run only when no exceptions are encountered in the try clause.  

6. Cleaning up After Using finally: After all your code is done and you want to clean up the work, we can use `finally`.  
    - Same three steps as above: `try, except, else`.  
    - `finally` Always run this code.  
        - Enables you to execute sections of code that should always run, with or without any previous encountered exceptions.  

## Additional Resources  
* [Read and Write Files in Python - Companion Video](https://realpython.com/courses/reading-and-writing-files-python/)  

## Bookmark/Skim
* [Reading and Writing Files in Python Quiz](https://realpython.com/quizzes/read-write-files-python/)  