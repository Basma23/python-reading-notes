# Classes and Objects

Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.

The baisc class we write it like this:

```
class MyClass:
    variable = "blah"

    def function(self):
    print("This is a message inside the class.")
```

# Thinking Recursively in Python

**Recursive Functions in Python**

A recursive function is a function defined in terms of itself via self-referential expressions.

This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.

**Maintaining State** 

When dealing with recursive functions, keep in mind that each recursive call has its own execution context, so to maintain state during recursion you have to either:

- Thread the state through each recursive call so that the current state is part of the current call’s execution context

- Keep the state in global scope

**Recursive Data Structures in Python**

A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. 

# Pytest Fixtures and Coverage

**Fixtures**

When you're writing tests, you're rarely going to write just one or two. Rather, you're going to write an entire "test suite", with each test aiming to check a different path through your code. In many cases, this means you'll have a few tests with similar characteristics, something that pytest handles with "parametrized tests".

But in other cases, things are a bit more complex. You'll want to have some objects available to all of your tests. Those objects might contain data you want to share across tests, or they might involve the network or filesystem. These are often known as "fixtures" in the testing world, and they take a variety of different forms.

In pytest, you define fixtures using a combination of the ```pytest.fixture``` decorator, along with a function definition.

