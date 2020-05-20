# Reading Notes 08  

## Articles  

### Primer on Generators  
* [Link to Article](https://realpython.com/primer-on-python-decorators/)  
- Decorators wrap a function, modifying its behavior.  
- Python allows you to use decorators in a simple way with an `@` symbol.  
- You can store your Python Decorators in there own `decorators.py` file.
    - Uses the import style of handling this: `from decorators import function()`  
- Keep in mind that wrapper functions might not take arguments but the function you decorate might have them.  
    - In your decorator function you need to implement `*args and **kwargs`  that will accept an arbitrary number of positional and keyword arguments.  
- Make sure the wrapper function returns the return value of the decorated function.  
- Decorators can be used on many things:  
    - Decorators on classes  
    - Several decorators on one function  
    - Decorators with arguments  
    - Decorators that can optionally take arguments  
    - Stateful decorators  
    - Classes as decorators
- Key Notes:
    - They can be reused over and over.  
    - They can decorate functions with arguments and return values.  
    - They can use `@functools.wrap` to look more like the decorated function.  
    - Touched the idea of nested decorators.  
    - Ability to add arguments to decorators.  
    - Keep/maintain state with decorator.  

### List Comprehensions  
* [Link to Article](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)  
* List Comprehensions  
- List comprehensions provide a concise way to create lists.  
    - It starts with with opening bracket followed by a for clause, then zero or more for or if clauses. The expression can be anything and ending with a bracket.
    - `new_list = [expression(i) for i in old_list if filter(i)]`  
    - `[expression for item in list if conditional ]`  
- Example Code:  This example how to convert a list from uppercase to lower and vice versa
```py
>>>[x.lower() for x in ["A", "B", "C"]]
['a', 'b', 'c']

>>> [x.upper() for x in ["a","b","c"]]
['A', 'B', 'C']
```

## Additional Resources  
* Listen(audio): [Debugging with PySnooper](https://www.pythonpodcast.com/pysnooper-python-debugging-episode-241/)  
