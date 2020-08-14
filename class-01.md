# Pain vs Suffering

**Pain** is what happens. 
**Suffering** is the story that we layer on top of what happens.

Pain is a normal, built-in part of life on earth. There’s no escaping it, so it’s pointless to resist it. It’s simply a fact that “good” things and “bad” things are always around the corner. What is avoidable, though, is suffering. All it takes is practice. 

# Beginners Guide to Big O notation

Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

**O(1)** describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.
**O(N)** describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set.
**O(N^2)** represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N3), O(N4) etc.
**O(2^N)** denotes an algorithm whose growth doubles with each additon to the input data set. The growth curve of an O(2N) function is exponential - starting off very shallow, then rising meteorically.

# Logarithms

Binary search is a technique used to search sorted data sets. It works by selecting the middle element of the data set, essentially the median, and compares it against a target value. If the values match it will return success. If the target value is higher than the value of the probe element it will take the upper half of the data set and perform the same operation against it. Likewise, if the target value is lower than the value of the probe element it will perform the operation against the lower half. It will continue to halve the data set with each iteration until the value has been found or until it can no longer split the data set.


This type of algorithm is described as O(log N). The iterative halving of data sets described in the binary search example produces a growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase e.g. an input data set containing 10 items takes one second to complete, a data set containing 100 items takes two seconds, and a data set containing 1000 items will take three seconds. Doubling the size of the input data set has little effect on its growth as after a single iteration of the algorithm the data set will be halved and therefore on a par with an input data set half the size. This makes algorithms like binary search extremely efficient when dealing with large data sets.

# How to Setup an Awesome Python Environment for Data Science or Anything Else

## The Python Environment
Pyenv is a set of three tools,  two of them are: pyenv (used to install python) and pyenv-virtualenv (used to configure your global tools).

## Dependency Management
Managing project dependencies in python can become messy or manual. 
Apart from many other things, poetry helps you to easily
manage your projects’ dependencies,
separate your projects through virtual environments,
build both applications as well as libraries without headaches.

