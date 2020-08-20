# Linked Lists

**What is a Linked List**
A Linked List is a sequence of ```Nodes``` that are connected/linked to each other. The most defining feature of a Linked List is that each ```Node``` references the next ```Node``` in the link.

There are two types of Linked List - Singly and Doubly. We will be implementing a Singly Linked List in this implementation.

**What does it look like**

![Linked List](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList1.PNG)

**Traversal**

When traversing a linked list, you are not able to use a ```foreach``` or ```for``` loop. We depend on the ```Next``` value in each node to guide us where the next reference is pointing. The ```Next``` property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.

The best way to approach a traversal is through the use of a ```while()``` loop. This allows us to continually check that the ```Next``` node in the list is not null. If we accidentally end up trying to traverse on a node that is ```null```, a ```NullReferenceException``` gets thrown and our program will crash/end.

When traversing through a linked list, the ```Current``` node is the most helpful. The ```Current``` will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.

**Big O**

The Big O of time for ```Includes``` would be O(n). This is because, at its worse case, the node we are looking for will be the very last node in the linked list. n represents the number of nodes in the linked list.

The Big O of space for ```Includes``` would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input.

## Linear data structures

If we really want to understand the basics of linked lists, it’s important that we talk about what type of data structure they are.

One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed. We can think of a linear data structure like a game of hopscotch: in order to get to the end of the list, we have to go through all of the items in the list in order, or sequentially. Linear structures, however, are the opposite of non-linear structures. In non-linear data structures, items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.

We might not always realize it, but we all work with linear and non-linear data structures everyday! When we organize our data into hashes (sometimes called dictionaries), we’re implementing a non-linear data structure. Trees and graphs are also non-linear data structures that we traverse in different ways, but we’ll talk more about them in more depth later in the year.
Similarly, when we use arrays in our code, we’re implementing a linear data structure! It can be helpful to think of arrays and linked lists as being similar in the way that we sequence data. 

**Memory management**

When an array is created, it needs a certain amount of memory. If we had 7 letters that we needed to store in an array, we would need 7 bytes of memory to represent that array. But, we’d need all of that memory in one contiguous block. That is to say, our computer would need to locate 7 bytes of memory that was free, one byte next to the another, all together, in one place.
On the other hand, when a linked list is born, it doesn’t need 7 bytes of memory all in one place. One byte could live somewhere, while the next byte could be stored in another place in memory altogether! Linked lists don’t need to take up a single block of memory; instead, the memory that they use can be scattered throughout.

**Parts of a linked list**

A linked list can be small or huge, but no matter the size, the parts that make it up are actually fairly simple. A linked list is made up of a series of nodes, which are the elements of the list.
The starting point of the list is a reference to the first node, which is referred to as the head. Nearly all linked lists must have a head, because this is effectively the only entry point to the list and all of its elements, and without it, you wouldn’t know where to start! The end of the list isn’t a node, but rather a node that points to null, or an empty value.

A single node is also pretty simple. It has just two parts: data, or the information that the node contains, and a reference to the next node.

**Lists for all shapes and sizes**

Even though the parts of a linked list don’t change, the way that we structure our linked lists can be quite different. Like most things in software, depending on the problem that we’re trying to solve, one type of linked lists might be a better tool for the job than another.
Singly linked lists are the simplest type of linked list, based solely on the fact that they only go in one direction. There is a single track that we can traverse the list in; we start at the head node, and traverse from the root until the last node, which will end at an empty null value.
But just as a node can reference its subsequent neighbor node, it can also have a reference pointer to its preceding node, too! This is what we call a doubly linked list, because there are two references contained within each node: a reference to the next node, as well as the previous node. This can be helpful if we wanted to be able to traverse our data structure not just in a single track or direction, but also backwards, too.

A circular linked list is a little odd in that it doesn’t end with a node pointing to a null value. Instead, it has a node that acts as the tail of the list (rather than the conventional head node), and the node after the tail node is the beginning of the list. This organization structure makes it really easy to add something to the end of the list, because you can begin traversing it at the tail node, as the first element and last element point to one another. Circular linked lists can start to get really crazy because we can turn both a singly linked list and a doubly linked list into a circular linked list!
But no matter how complicated a linked list is, if we can remember the fundamentals of a node and how it works and how the different pointer references in our list are structured, there’s no linked list we can’t tackle!

**What is Big O?**

One way to think about Big O notation is a way to express the amount of time that a function, action, or algorithm takes to run based on how many elements we pass to that function.
Some external factors affect the time it takes for a function to run: the speed of the processor, what else the computer is running, etc. So it’s hard to make strong statements about the exact runtime of an algorithm. Instead we use big O notation to express how quickly its runtime grows.

An O(1) function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm. An O(n) function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.
For a little contrast, we can also compare these two functions to something starkly different: an O(n²) function, which clearly takes exponentially more time. 

**Growing a linked list**
We can add elements and remove elements from a linked list by rearrange our pointers. We know that a linked list is made up a single node, and a node always contains some data and, most importantly, a pointer to the next node or null. So, all we need to do in order to add something to our linked list is figure out which pointer needs to point to where.
First, we find the head node of the linked list.
Next, we’ll make our new node, and set its pointer to the current first node of the list.

But inserting an element at the end of a linked list is a different story. The interesting thing here is that the steps you take to actually do the inserting are the exact same:
Find the node we want to change the pointer of (in this case, the last node)
Create the new node we want to insert and set its pointer (in this case, to null)
Direct the preceding node’s pointer to our new node
However, there’s an added complexity here: we’re not adding something to the beginning of the list, at the head node. Nope — instead, we’re adding something after the last node. So we will need to find the last node. Which means that we’ll need to traverse through the entire linked list to find it. And we know that linked lists are distributed, non-contiguous in memory.
A good rule of thumb for remember the characteristics of linked lists is this:
a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element.


