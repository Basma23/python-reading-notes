# Dunder (Magic, Special) Methods

**What Are Dunder Methods?**

In Python, special methods are a set of predefined methods that we can use to enrich our classes. They are easy to recognize because they start and end with double underscores, such as ```__init__ ```or``` __str__```.

These “dunders” or “special methods” in Python are also sometimes called “magic methods.” 

Dunder methods let us emulate the behavior of built-in types. 

**Special Methods and the Python Data Model**

This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, attribute access, etc.

We can see Python’s data model as a powerful API you can interface with by implementing one or more dunder methods. If we want to write more Pythonic code, knowing how and when to use dunder methods is an important step.

**Object Initialization: __init__**

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

**Object Representation: ```__str__```, ```__repr__```**

It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

```__repr__```: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

```__str__```: The “informal” or nicely printable string representation of an object. This is for the enduser.

# Basic Statistics in Python — Probability

**What is probability?** 

An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur.

 To calculate the probability of an event occurring, we count how many times are event of interest can occur and dividing it by the sample space. By looking at the events that can occur, probability gives us a framework for making predictions about how often events will happen. We can gather data! We can use statistics to calculate probabilities based on observations from the real world and check how it compares to the ideal.