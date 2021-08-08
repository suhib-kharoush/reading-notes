# Enriching Your Python Classes With Dunder (Magic, Special) Methods

##### What Are Dunder Methods?

- In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

- Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:
```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
```

- To fix this, you can add a __len__ dunder method to your class:
```
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```

##### Object Initialization: __init__

- Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:
```
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []
```

##### Object Representation: __str__, __repr__

- - __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

- - __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.


# Python Iterators: A Step-By-Step Introduction

##### How do for-in loops work in Python?
- How do for-in loops work in Python?
```
repeater = Repeater('Hello')
for item in repeater:
    print(item)
```

##### A Simpler Iterator Class

- Up until now our iterator example consisted of two separate classes, Repeater and RepeaterIterator.

##### Who Wants to Iterate Forever

- At this point you’ll have a pretty good understanding of how iterators work in Python. But so far we’ve only implemented iterators that kept on iterating forever.

##### Python 2.x Compatible Iterators

- All the code examples I showed here were written in Python 3. There’s a small but important difference between Python 2 and 3 when it comes to implementing class-based iterators:
- - In Python 3, the method that retrieves the next value from an iterator is called __next__.
- - In Python 2, the same method is called next (no underscores)

##### What Are Python Generators?
- Python Generators 101 – The Basics


##### Python Generators – A Quick Summary
- - Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.
- - The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.
- - Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.