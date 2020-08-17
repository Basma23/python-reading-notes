# Python Modules and Packages

**Modular programming** refers to the process of breaking a large, unwieldy programming task into separate, smaller, more manageable subtasks or modules. Individual modules can then be cobbled together like building blocks to create a larger application.


**Advantages to modularizing code in a large application:**

- **Simplicity:** Rather than focusing on the entire problem at hand, a module typically focuses on one relatively small portion of the problem. If you’re working on a single module, you’ll have a smaller problem domain to wrap your head around. This makes development easier and less error-prone.

- **Maintainability:** Modules are typically designed so that they enforce logical boundaries between different problem domains. If modules are written in a way that minimizes interdependency, there is decreased likelihood that modifications to a single module will have an impact on other parts of the program. (You may even be able to make changes to a module without having any knowledge of the application outside that module.) This makes it more viable for a team of many programmers to work collaboratively on a large application.

- **Reusability:** Functionality defined in a single module can be easily reused (through an appropriately defined interface) by other parts of the application. This eliminates the need to duplicate code.

- **Scoping:** Modules typically define a separate namespace, which helps avoid collisions between identifiers in different areas of a program. (One of the tenets in the Zen of Python is Namespaces are one honking great idea—let’s do more of those!)


**There are actually three different ways to define a module in Python:**

- A module can be written in Python itself.
- A module can be written in C and loaded dynamically at run-time, like the re (regular expression) module.
- A built-in module is intrinsically contained in the interpreter, like the itertools module.


**A module’s contents are accessed the same way in all three cases: with the import statement.**

**import** statement, it searches for python file in a list of directories assembled from the following sources:

- The directory from which the input script was run or the current directory if the interpreter is being run interactively
- The list of directories contained in the PYTHONPATH environment variable, if it is set. (The format for PYTHONPATH is OS-dependent but should mimic the PATH environment variable.)
- An installation-dependent list of directories configured at the time Python is installed


**Module contents are made available to the caller with the import statement, an it takes many different forms.**


# pytest


**What is PyTest?**
Pytest is a testing framework which allows us to write test codes using python. You can write code to test anything like database , API, even UI if you want. But pytest is mainly being used in industry to write tests for APIs.

**Why use PyTest?**

Some of the advantages of pytest are

- Very easy to start with because of its simple and easy syntax.
- Can run tests in parallel.
- Can run a specific test or a subset of tests
- Automatically detect tests
- Skip tests
- Open source


# Recursion


**What is Recursion?**

The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily. 

**What is base condition in recursion?**

In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems.

**How a particular problem is solved using recursion?**

The idea is to represent a problem in terms of one or more smaller problems, and add one or more base conditions that stop the recursion.

**Why Stack Overflow error occurs in recursion?**

If the base case is not reached or not defined, then the stack overflow problem may arise.
