# What Are Dunder Methods?

- In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

## Special Methods and the Python Data Model:
- This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, attribute access, etc.

- Throughout this article I will enrich a simple Python class with various dunder methods to unlock the following language features:
- - Initialization of new objects.
- - Object representation
- - Enable iteration
- - Operator overloading (comparison)
- - Operator overloading (addition)
- - Method invocation
- - Context manager support (with statement)

## Object Initialization: __init__:
- Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:

## Object Representation: __str__, __repr__
- It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:
- - __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.
- - __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

# Basic Statistics in Python — Probability:

- What is probability?
- The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:
1. Flipping a heads
2. Flipping a tails

