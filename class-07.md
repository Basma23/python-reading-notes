# Python Scope & the LEGB Rule

**Understanding Scope**

In programming, the scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects, and so on. A name will only be visible to and accessible by the code in its scope. Several programming languages take advantage of scope for avoiding name collisions and unpredictable behaviors. There are two general scopes, and they are:

- **Global scope:** The names that you define in this scope are available to all your code.

- **Local scope:** The names that you define in this scope are only available or visible to the code within the scope.

Scope came about because early programming languages only had global names. With this kind of name, any part of the program could modify any variable at any time, so maintaining and debugging large programs could become a real nightmare. To work with global names, you’d need to keep all the code in mind at the same time to know what the value of a given name is at any time. This was an important side-effect of not having scopes.

**Python** use the scope to avoid this kind of problem. When using a domain implementation language, there is no way for us to access all variables in the program at all locations in that program. In this case, our ability to access a particular name will depend on where we specified that name.

The names in our programs will have the ***scope*** of the block of code in which we define them. When we can access the value of a given name from someplace in our code, we’ll say that the name is ***in scope***. If we can’t access the name, then we’ll say that the name is ***out of scope***.

Python uses the location of the name assignment or definition to associate it with a particular scope. So, where we assign or define a name in our code we determine the scope or visibility of that name, such as  if we assign a value to a name inside a function, then that name will have a **local Python scope**, but if we assign a value to a name outside of all functions, such as at the top level of a module—then that name will have a **global Python scope**.

**Python Scope vs Namespace** 

In Python, the concept of scope is closely related to the concept of the namespace. **Python scope** determines where in our program a name is visible. **Python scopes** are implemented as dictionaries that map names to objects. These dictionaries are commonly called **namespaces**. These are the concrete mechanisms that Python uses to store names, where they’re stored in a special attribute called ```.__dict__```.

Using the LEGB Rule for Python Scope
Python resolves names using the so-called LEGB rule, which is named after the Python scope for names. The letters in LEGB stand for Local, Enclosing, Global, and Built-in.

- **Local (or function) scope is:** the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. It’s created at function call, not at function definition, so you’ll have as many different local scopes as function calls. This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.

- ***Enclosing (or nonlocal) scope is:** a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

- **Global (or module) scope is:** the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

- **Built-in scope is:** a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.

The LEGB rule is a kind of name lookup procedure, which determines the order in which Python looks up names. So, if we reference a given name, then Python will look that name up sequentially in the local, enclosing, global, and built-in scope. If the name exists, then we’ll get the first occurrence of it. Otherwise, we’ll get an error.

**Functions: The Local Scope**
The local scope or function scope is a Python scope created at function calls. Every time we call a function, we’re also creating a new local scope. On the other hand, we can think of each def statement and lambda expression as a blueprint for new local scopes. These local scopes will come into existence whenever we call the function at hand.

By default, parameters and names that we assign inside a function exist only within the function or local scope associated with the function call. When the function returns, the local scope is destroyed and the names are forgotten.

**Nested Functions: The Enclosing Scope**

***Enclosing or nonlocal scope*** is observed when you nest functions inside other functions. It takes the form of the local scope of any enclosing function’s local scopes. Names that we define in the enclosing Python scope are commonly known as **nonlocal names**.

**Modules: The Global Scope**

From the moment we start a Python program, we’re in the global Python scope. Internally, Python turns our program’s main script into a module called ```__main__``` to hold the main program’s execution. The namespace of this module is the main global scope of our program.

**Builtins: The Built-In Scope**

The built-in scope is a special Python scope that’s implemented as a standard library module named builtins. All of Python’s built-in objects live in this module. They’re automatically loaded to the built-in scope when you run the Python interpreter. Python searches builtins last in its LEGB lookup, so you get all the names it defines for free. This means that you can use them without importing any module.


