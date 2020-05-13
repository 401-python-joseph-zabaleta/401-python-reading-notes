# Reading Notes 04
- [Table of Contents](README.md)
## Articles  

### Classes and Objects  
* [Link to Article](https://www.learnpython.org/en/Classes_and_Objects)  
Objects are encapsulation of variables and functions into a single entity.  
    - Objects get their variables and functions from classes.  
    - Classes are essentially a template to create your objects.  

    ```py
        class MyClass:
            variable="blah"

            def function(self):
                print("This is a message inside the class")

        myobjectx = MyClass()
        myobjectx.variable
        myobjectx.function()
    ```
    - You can create multiple different objects that are of the same class. Each object will contain independent copies of the variables defined in that class.
    - Accessing a variable we use the dot notation.  
    - Accessing a function we use the dot notation as well.  

### Thinking Recursively (Optional: "Naive Recursion is Naive" section and beyond)  
* [Link to Article](https://realpython.com/python-thinking-recursively/)  
1. Dear Pythonic Santa Clause...
    - An explicit loop, loop construction is called an iterative algorithm.
    - Loops one way until its finished.  
    - A typical structure for a recursive solution or algorithm: If a current prolbem represents a small case, solve it. If not, divide it into subproblems and apply the same strategy to them.  
2. Recursive Functions in Python  
    - A recursive function is a function defined in terms of itself via self-referential expressions.  
    - Meaning it will continuously call itself over and over until a condition is met.  
    - All recursive functions share a common structure made of two parts:  
        - Base case  
        - Recursive case  
    - Example of calculated `n!` using a recursive function:  
    ```py
    def factorial_recursive(n):
        # Base Case: 1! = 1
        if n == 1:
            return 1
        
        # Recursive case: n! = n * (n-1)!
        else:
            return n * factorial_recursive(n-1)
    ```
3. Maintaining State  
    - Recursive functions have their own execution context, so to maintain state during recursion you have to either:  
        - Thread the state through each recursive call so that the current state is part of the current call's execution context.  
            ```py
                def sum_recursive(current_number, accumulated_sum):
                    # Base case
                    # Return the final state
                    if current_number == 11:
                        return accumulated_sum

                    # Recursive case
                    # Thread the state through the recursive call
                    else:
                        return sum_recursive(current_number + 1, accumulated_sum + current_number)
                    
                    # Pass the initial state
                    >>> sum_recursive(1,0)  
                    55
            ```
        - Keep the state in global scope.  
            ```py
            # Global mutable state
            current_number = 1
            accumulated_sum = 0


            def sum_recursive():
                global current_number
                global accumulated_sum
                # Base case
                if current_number == 11:
                    return accumulated_sum
                # Recursive case
                else:
                    accumulated_sum = accumulated_sum + current_number
                    current_number = current_number + 1
                    return sum_recursive()
            ```
4. Recursive Data Structures in Python  
    - A data structure is recursive if it can be defined in terms of a smaller version of itself.  
    - Some types of data structures are:  
        - Lists
        - set  
        - tree  
        - dictionary  
    
    - Both recursive functions and data structures go together.  
    - The recursive function’s structure can often be modeled after the definition of the recursive data structure it takes as an input

5. Naive Recursion is Naive  
    - Fibonacci numbers were originally defined by the Italian mathematician Fibonacci in the thirteenth century to model the growth of rabbit populations.  
    - To count the number of rabbits born in the nth year, he defined this recurrence relation:  
    f<sub>n</sub> =  f<sub>n-1 </sub> + f<sub>n-2</sub>
    - This is a rather inefficient way of calculating large nth years. A better way is using or caching results of each Fibonaccci computations. See example code block below:  
    ```py
    from functools import lru_cache

    @lru_cache(maxsize=None)
    def fibonacci_recursive(n):
        print("Calculating F", "(", n, ")", sep="", end=", ")

        # Base case
        if n == 0:
            return 0
        elif n == 1:
            return 1

        # Recursive case
        else:
            return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)
    ```
    - To learn more about this take a look into functools, and lru_cache  
6. Pesky Details  
    - Python does not support tail-call elimination. This results in a stack overflow if you end up using more stack frames than the default call stack depth.  
    - Keep this in mind if you have a program that requires deep recursion.  
7. Fin
    - Author was asked to explain recursion in an interview. He took a piece of paper and wrote "Please turn over" on both sides. This is a great joke! Its just calling on itself over and over to turn over!

### Pytest Fixtures and Coverage  
* [Link to Article](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)  
1. Fixtures  
    - When writing tests we tend to write more than one, this is called a test suite.  
    - Tests that can be grouped in similairity are "parametrized tests"  
    - In pytest we define fixtures using the `pytest.fixture` decorator.  
    - We can create fixtures like this below:  
        ```py
        @pytest.fixture
        def simple_file():
        return StringIO('\n'.join(['abc', 'def', 'ghi', 'jkl']))
        ```
    - Next we can pass this fixture into a test function like so:  
        ```py
        def test_reverse_lines(simple_file):
            assert reverse_lines(simple_file) == ['cba\n', 'fed\n','ihg\n', 'lkj\n']
        ```
    - Fixtures run once per test that calls it unless given additional conditions.  
        - `scope` parameter sets the availability of that fixture to our tests.  
2. Coverage  
    - This is talking about how thoroughly you test your code. Can you ensure that all paths through your functions have been tested?  
    - There is a package called `pytest-cov` which can be called `pytest --cov` I will need to follow up with more information after learning hands on how this all works.  

#### Resources from Article  
- [pytest Website](https://docs.pytest.org/en/latest/)  
- [Python testing with pytest Book by Pragmatic Programmers](https://pythontesting.net/)  
  
  
## Bookmark/Skim
* [Pytest Fixtures](https://docs.pytest.org/en/latest/fixture.html)  