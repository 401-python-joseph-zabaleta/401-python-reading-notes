# Reading Notes 07  

## Articles  
### Python Scope & the LEGB Rule: Resolving Names in Your Code
* [Link to Article](https://realpython.com/python-scope-legb-rule/)  

Understanding Scope  
- Global Scope: The names that you define in this scope are available to all your code.  
- Local Scope: The names that you define in this scope are only available or visible to the code within the scope.  

Using Scope Related Built-In Functions  
- `global()`: is a built-in function that returns a reference to the current global scope or namespace dictionary.  
    - This means if you call `global()` it will return a dictionary of all currently available global variables.  
- `locals()`: is a built-in function that updates and returns a dictionary that holds a copy of the current state of the local python scope or namespace.  
    - THis means if you call `locals()` in a function block, you get all the names assigned in the local scope up to the point where you called `locals()`.  

## Bookmark/Skim
### Rolling Dice Examples  
* [Link to Article](https://artofproblemsolving.com/wiki/index.php/Basic_Programming_With_Python#Program_Example_1_3)  

### Random: Program Example 1
There is a package in Python that allows the user of random numbers.  

Generate a random number from 1 to 6.  
```py
import random
print(random.randint(1,6))
```

### Random: Program Example 2  
Simulate the rolling of 1000 dice. Now, count the number times you roll 6. Print that number out.  

```py
import random
count = 0

def roll():
    return random.randint(1,6)

for i in range(1, 1001):
    if roll() == 6
        count += 1
```

### Random: Program Example 3  
Simulate the rolling of 10,000 dice. Now, count the amount of times you roll 3. Print that amount out.  

```py
import random 

def roll():
    return random.randint(1,6)

def count(amount):
    count_ = 0

    for i in range (1, amount+1):
        if roll() == 3:
            count_ += 1
    return count_

print(count(10000))
```

### Random: Program Example 4  
One of my friends loves rolling dice. He is going to roll 1 die tomorrow, 2 dice two days from now, 3 dice three days from now, and so on so that he rolls $a$ dice $a$ days from now. He gets tired rolling dice after rolling dice for 365 days (so the last day he rolls 365 dice). In Python, simulate this. How many times does he roll 3 after 365 days of rolling dice?

```py
import random

def roll():
    return random.int(1,6)

def count(amount):
    count_ = 0
    for i in range(1, amount+1):
        if roll() == 3:
            count_ += 1
    return count_

total = 0

for i in range(1, 366):
    total += count(i)

print(total)
```

### Random: Program Example 5  
20 of my friends love rolling dice. They are all going to roll 1 die each tomorrow, 2 dice each two days from now, 3 dice each three days from now, and so on so that they roll $a$ dice each $a$ days from now. But, one of my friends gets tired very quickly and he only rolls dice for 1 day and stops. Another friend only will roll dice for 2 days, and another will roll dice for three days only, and so on up to the fact that my last friend will roll dice for 20 days. In Python, simulate this. How many times does someone roll 3 after everything

```py
import random

def roll()
    return random.int(1,6)

def count(amount):
    count_ = 0
    for i in range(1, amount + 1):
        if roll() == 3:
            count_ += 1
    return count_

def count2(amount):
    total = 0
    for i in range(1, amount + 1):
        total += count(i)
    return total

def count3(amount):
    total = 0
    for i in range(1, amount + 1):
        total += count2(i)
    return total

print(count3(20))
```

## Videos  

### Don't be CONFUSED by BIG O notation anymore!
* [Link to Video](https://www.youtube.com/watch?v=5Uqawfl0VHQ)  
