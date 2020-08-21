# How to use the Random Module in Python

The **random module** provides access to functions that support many operations. Perhaps the most important thing is that it allows us to generate random numbers.

**Random functions**

The Random module contains some very useful functions.

```
import random
print random.randint(0, 5)
```

To get the larger number randomly just multiply it.

```
import random
random.random() * 100
```
**Choice**

Generate a random value from the sequence sequence.

The choice function can often be used for choosing a random element from a list.

```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

**Shuffle**

The shuffle function, shuffles the elements in list in place, so they are in a random order.

```
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
```

**Randrange**

Generate a randomly selected element from range(start, stop, step)

```
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```
