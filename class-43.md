# Reading Notes 43  

## Articles  

### Dunder Methods
* [Link to Article](https://dbader.org/blog/python-dunder-methods)  

Dunder methods:  
- Special set of methods predefined to enrich your classes.  
- for example `__init__` or `__str__`
- This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, attribute access, etc.

Some features you can gain from dunder methods are:  
- Initialization of new objects  
- Object representation  
- Enable iteration  
- Operator overloading (comparison)  
- Operator overloading (addition)  
- Method invocation  
- Context manager support  

### Iterators  
* [Link to Article](https://dbader.org/blog/python-iterators)  

There were a few examples to follow to learn about iterators in python. Here was the quick summary:  
- Iterators provide a sequence interface to Python objects that’s memory efficient and considered Pythonic. Behold the beauty of the for-in loop!  
- To support iteration an object needs to implement the iterator protocol by providing the __iter__ and __next__ dunder methods.   
- Class-based iterators are only one way to write iterable objects in Python. Also consider generators and generator expressions.  


### Generators  
* [Link to Article](https://dbader.org/blog/python-generators)  
- Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.  
- The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.  
- Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.

## Addtional Resources  

### Videos 
* [What are Generators](https://realpython.com/lessons/what-are-python-generators/)  

## Bookmark/Skim  
* [Decorators](https://realpython.com/primer-on-python-decorators/)  