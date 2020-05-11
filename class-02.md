# Reading Notes 02

## Articles  

### Python Modules and Packages  
* [Link to Article](https://realpython.com/python-modules-packages/)  
This article explores Python modules and Python Packages, two mechanisms that facilitate modular programming.  

* Modular programming is the process of breaking a large program into smaller more managable parts. Advantages to modularizing are:
    - Simplicity  
    - Maintainability  
    - Reusability  
    - Scoping  

1. Python Modules: Overview  
A module can be accessed with an `import` statement. Modules written in Python are just a name with a .ey extension.  

2. The module Search Path    
When the inerpreter executes the `import` statement it searchs for the module in a list of directories assembled from the following sources:  

    - Current Directory  
    - List of directories contained in the PYTHONPATH environment variable  
    - Installation-Dependent list of directories configured at the time Python is installed  

3. The `import` Statement  
Module contents are made available to the caller with the `import` statement. The `import` statement takes many different forms.  

    - `import <module name>`  
        - Each module has its own private symbol table.  
        - From the caller, objects in the module are only accessible using `dot notation`.  
    - `from <module name> import <name(s)>`  
        - Adds module object name to caller's symbol table.  
        - This will import specific objects  
        - You can refer to them by name without `dot notation`.  
    - `from <module name> import * `  
        - Same as above but now we are import all objects in module  
    - `from <module name> import <name> as <alt name>`  
        - We can import specific parts of module and change there local name.  
    
4. The `dir()` Function  
The built-in function `dir()` returns a list of defined names in a namespace. Without arguments, it produces an alphabetically sorted list of names in the current local symbol table.  

    - When given an argument that is the name of a module, `dir()` lists the names defined in that module: example: `dir(module name)`.  

5. Executing a Module as a Script  
Any .py file that contains a module is essentially also a Python Script. 

    - When importing modules Python sets a `dunder` variable to `__name__` of module.  
    - If its a standalone script file , the `dunder` variable is set to a string `__main__`.  
    - Modules are often designed with the ability to run as a standalone script for testing purposes. This is refered to as `unit testing`.  

6. Reloading a Module  
For reasons of efficiency, a module is only loaded once per interpreter session. 
    - If you make a change to a module and require a reload. You need to either restart the interpreter or us a function called `reload()` from the module `importlib`.  

7. Python Packages  
As number of modules grow, its hard to keep track of them if they are saved in one location. We can organize them using packages.  

    - `Packages`: allow for a hierarchical structuring of the module namespace using `dot notation`.  
    - Creating a package is like creating a folder to hold your modules.  
    - `import <module name>[module inside a folder]`  

8. Package Initialization  
If a file anemd `__init__.py` is present in a package directory, it is invoked when that package or module in the package is imported.  
Starting with Python 3.3, Implicit Namespace Packages were introduced. These allow for the creation of a package without any __init__.py file. Of course, it can still be present if package initialization is needed. But it is no longer required.  

9. Importing * From a Package  
This is does not work the same as importing module *. There are slight differences in how this works.  You can add `__all__` set to a list of all the modules in a package inside an `__init__.py` file.  

    `__all__` Can be used in both packages and modules to control what is imported when import * is specified.  

    - For a package, when `__all__` is not defined, import * does not import anything.  
    - For a module, when `__all__` is not defined, import * imports everything(except names starting with an underscore)  

10. Subpackages  
Packages can contain nested `subpackages` to arbitrary depth. The Syntax is similiar to that of packages but additional `dot notation` is required.  

    - example: `import pkg.sub_pkg1.mod1` 
    - A module in one `subpackage` can references objects in `sibling subpackages`  
    - Two ways to import are `absolute import` and `relative import`.  

### Pytest Documentation  
* [Link to Article](https://docs.pytest.org/en/latest/)  
The `pytest` framework makes it easy to write small tests, yet scales to support complex functional testing for applications and libraries.

### PyTest Tutorial (Up to Section Running tests in parallel)  
* [Link to Article](https://www.guru99.com/pytest-tutorial.html)  
Some Advantages of `pytest` are:  

    - Very easy to start with because of its simple and easy syntax  
    - Can run tests in parallel  
    - Can run a specific test or a subset of tests  
    - Automatically detect tests  
    - Skip tests  
    - Open Sources  

    First you must install `pytest`
    
    - `pip install pytest==2.9.1`  
    - Verify with `py.test -h`  
    - Install pytest-xdist for running tests in parallel  
    - `pip install pytest-xdist`  

    Test Commands:  
    
    - `py.test`
    - `py.test filename.py`  
    - `py.test -k substring to match -v`  
    - `py.test -m name-of-mark`  
    - `py.test -n 4`  

### Recursion  
* [Link to Article](https://www.geeksforgeeks.org/recursion/)  
Recursion: The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function.  

## Additional Resources
* [Python Modules and Packages Companion](https://realpython.com/courses/python-modules-packages/)  

## Bookmark/Skim  
* Google for Education:
    - [Python Lists](https://developers.google.com/edu/python/lists)  
    - [Python Strings](https://developers.google.com/edu/python/strings)  
