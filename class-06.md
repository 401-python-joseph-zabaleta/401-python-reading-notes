# Reading Notes 06

## Articles  

### How to use Random Module  
* [Link to Article](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)  
1. Overview  
    - The random module provides access to functiosn that support many operations.  
    - An important function is the Generatee random numbers.  
2. When to Use it?  
    - Looking for a random number in a given range.  
    - Pick a random element from a list, from a deck, flip a coin.  
    - Making password databases more secure or powering up a random page feature.  
3. Random Functions  
    - `randint function` for random integers  
        - accepts two parameters: a lowest and highest number.  
        - Generates a random integer in the range.  
    - `random function` if you want a larger number you can multiply it.  
        - `random.random() * 100`  
    - `choice function` generates random value from the sequence  
        - often the function of choice for choosing a random element from a list. (pun)  
    - `shuffle function` can shuffle a list into a random order.  
        - `random.shuffle(list)`  
    - `Randrange` randomly selected element from a range(start, stop, step)  
    
### What is Dependecy Injection  
* [Link to Article](https://www.freecodecamp.org/news/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-7578c84fa88f/)  
1. Introduction  
    - In software engineering, dependency injection is a technique whereby one object (or static method) supplies the dependencies of another object. A dependency is an object that can be used( a service).  

2. Why should I use dependency injection?  
    - Dependency injection can be thought as the middleman. Creating objects for a provided oject or class.  
    - Making a class or object independant from creating objects.  

3. There are basically three types of dependency injection:  
    - `Constructor injection:` the dependencies are provided through a class constructor.  
    - `settle injection:` the client exposes a settle method that the injector uses to inject the dependency.  
    - `interface injection:` the dependency provides an injector method that will inject the dependency into any client passed to it. Clients must implement an interface that exposes a `setter method` that accepts the dependency.   

    - Dependency Injection's reponsibilities:  
        - Create the objects.  
        - Know which classes require those objects  
        - Provide them all those objects.  

4. Inversion of Control  
    - This states that a class should not configure its dependencies statically but should be configured by some other class from outside.  
    - Fifth principle of S.O.L.I.D. check more here [SOLID by Uncle Bob](https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design#toc-single-responsibility-principle)  

5. Pros and Cons  
    - Benefits of using DI:  
        - Helps in Unit testing.  
        - Boiler plate code is reduced, as initializing of dependencies is done by the injector component.  
        - Extending the application becomes easier.  
        - Helps to enable loose coupling, which is important in applcation programming.  

    - Disadvantages of DI:  
        - It's a bit complex to learn and if overused can lead to management issues and other problems.  
        - Many compile time errors are pushed to run-time.  
        - Dependency injection frameworks are implemented with reflection or dynamic programming. This can hinder use of IDE automation, such as "find references", "show hierarchy" and safe refactoring.  

6. Libraries and Frameworks that implement DI  
    - Spring(JAVA)  
    - Google Guide(JAVA)  
    - Dagger(JAVA and Andriod)  
    - Castle Windsor (.NET)  
    - Unity(.NET)  


## Videos  

### Big O Notation  
* [Link to Video](https://www.youtube.com/watch?v=v4cd1O4zkGw)  


## Bookmark/Skim
* [Python Random](https://docs.python.org/3/library/random.html)  