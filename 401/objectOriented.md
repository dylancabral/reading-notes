# Object orianted programming

## Classes and Objects

classes can be summarized as templates to create objects

self is a paramter refering to an instance of an class object

You can create multiple different objects that are of the same class(have the same variables and functions defined). However, each object contains independent copies of the variables defined in the class

To access a function inside of an object you use notation similar to accessing a variable:

```python

class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()

myobjectx.function()
```

The __init__() function, is a special function that is called when the class is being initiated. It's used for assigning values in a class.

## Thinking recursively

how to cache results [Caching Results](https://realpython.com/python-memcache-efficient-caching/)

![recursion diagram](/images/recursiondiagram.jpg)

## The algorithm for recursive present delivery implemented in Python:

```python
houses = ["Eric's house", "Kenny's house", "Kyle's house", "Stan's house"]

# Each function call represents an elf doing his work 
def deliver_presents_recursively(houses):
    # Worker elf doing his work
    if len(houses) == 1:
        house = houses[0]
        print("Delivering presents to", house)

    # Manager elf doing his work
    else:
        mid = len(houses) // 2
        first_half = houses[:mid]
        second_half = houses[mid:]

        # Divides his work among two elves
        deliver_presents_recursively(first_half)
        deliver_presents_recursively(second_half)
```

## What is Recursion

Now that we have some intuition about recursion, let’s introduce the formal definition of a recursive function. A recursive function is a function defined in terms of itself via self-referential expressions.

recursion involves calling on itself until it realizes the expected or asked result

You need a base case and a Recursive case

Recursive function for calculating n in the python program

```python
def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)

```

## How to maintain state with recursive functions

- Thread the state through each recursive call so that the current state is part of the current call’s execution context
- Keep the state in global scope

## how to know if a data structure is recursive

A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. A list is an example of a recursive data structure

If a output ca
![Recursive](/images/recursively.jpg)

## Pytest fixes and coverage

you define fixture in ptest by coding pytest.fixture decorator and a function definition

fixtures allow you to provide your test with the appropriate object at the right time.

```pytest
@pytest.fixture
def simple_file():
   return StringIO('\n'.join(['abc', 'def', 'ghi', 'jkl']))

```

these are used differently than global variables you can call upon these specifically 

you can call upon fixtures like a function over and over where they are needed because under the hood they are set up like functions

 If your fixture uses "yield" instead of "return", pytest understands that the post-yield code is for tearing down objects and connections.if your fixture has "module" scope, pytest will wait until all of the functions in the scope have finished executing before tearing it down.

## Pytest-cov on pypi

this is a package that you can use to run the --cov option on your tests if you dont specify you will get a coverage report of every part of the python library this program is using, coverage meaning its testing all possible inputs for return or you can specify what librarys to test

you can turn this coverage report into html so that humans can understand it and this can be done with this package

```pytest

coverage html
```

This creates a directory called htmlcov. Open the index.html file in this directory using your browser, and you'll get a web-based report showing (in red) where your program still lacks coverage

## Things I Want To Know More About

## Resources

[Classes and Objects](https://www.learnpython.org/en/Classes_and_Objects)

[Thinking Recursively](https://realpython.com/python-thinking-recursively/)

[Pytest Fixtures and Coverage](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)

[Pytest website](http://pytest.org/)

[A book on the subject](http://pythontesting.net/)

[blog post about pytest fixtures](http://pythontesting.net/framework/pytest/pytest-fixtures-nuts-bolts)