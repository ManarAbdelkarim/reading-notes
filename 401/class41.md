# Readings: Pythonisms

## Enriching Your Python Classes With Dunder (Magic, Special) Methods

What Are Dunder Methods?
In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

### Object Initialization: __init__
Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder

### Object Representation: __str__, __repr__
It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

__repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

### Iteration: __len__, __getitem__, __reversed__
In order to iterate over our account object I need to add some transactions. So first, I’ll define a simple method to add transactions. I’ll keep it simple because this is just setup code to explain dunder methods, and not a production-ready accounting system.

## Python Iterators: A Step-By-Step Introduction

### How do for-in loops work in Python?
At this point we’ve got our Repeater class that apparently supports the iterator protocol, and we just ran a for-in loop to prove it:

        repeater = Repeater('Hello')
        for item in repeater:
            print(item)
Now, what does this for-in loop really do behind the scenes? How does it communicate with the repeater object to fetch new elements from it?

To dispel some of that “magic” we can expand this loop into a slightly longer code snippet that gives the same result:

        repeater = Repeater('Hello')
        iterator = repeater.__iter__()
        while True:
            item = iterator.__next__()
            print(item)


## What Are Python Generators?

Generators are a tricky subject in Python. With this tutorial you’ll make the leap from class-based iterators to using generator functions and the “yield” statement in no time.

- Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.

- The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.

- Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.