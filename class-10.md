# What is a Stack

A stack is a data structure that consists of ```Nodes```. Each ```Node``` references the next Node in the stack, but does not reference its previous.

Stacks follow these concepts:

**FILO**

First In Last Out

This means that the first item added in the stack will be the last item popped out of the stack.

**LIFO**

Last In First Out

This means that the last item added to the stack will be the first item popped out of the stack.

**Stack Visualization**

Push:

![Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)

![Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack1.PNG])

![Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/pushStack2.PNG)

![Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

Pop:

![Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack1.PNG)

![Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack2.PNG)

![Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack3.PNG)

![Stack Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/popStack4.PNG)

Peek:

When conducting a ```peek```, you will only be inspecting the ```top``` Node of the stack.

Typically, you would check ```isEmpty``` before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

We do not re-assign the ```next``` property when we ```peek``` because we want to keep the reference to the next Node in the stack. This will allow the ```top``` to stay the top until we decide to ```pop```.

IsEmpty:

```
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return top = NULL
```

# What is a Queue

Queues follow these concepts:

**FIFO**

First In First Out

This means that the first item in the queue will be the first item out of the queue.

**LILO**

Last In Last Out

This means that the last item in the queue will be the last item out of the queue.

**Queue Visualization**

![Queue Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)

Enqueue:

![Queue Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Enqueue1.PNG)

![Queue Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Enqueue2.PNG)

![Queue Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Enqueue3.PNG)

Dequeue:

![Queue Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Dequeue1.PNG)

![Queue Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Dequeue2.PNG)

![Queue Visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Dequeue3.PNG)

Peek:

When conducting a ```peek```, you will only be inspecting the ```front``` Node of the queue.

Typically, you want to check ```isEmpty``` before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.

IsEmpty:

```
ALGORITHM isEmpty()
// INPUT <-- none
// OUTPUT <-- boolean

return front = NULL
```