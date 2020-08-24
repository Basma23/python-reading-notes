# List Comprehensions in Python

**List comprehensions** provide a concise way to create lists.

It consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses. 

The expressions can be anything, so we can put in all kinds of objects in lists.

The result will be a new list resulting from evaluating the expression in the context of the for and if clauses which follow it.

The **list comprehension** always returns a **result list**.

## Syntax

The basic syntax uses square brackets.

```
[ expression for item in list if conditional ]
```

It's equivalent to:
```
for item in list:
    if conditional:
        expression
```

