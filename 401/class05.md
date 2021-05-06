# Implementation: Linked Lists
![](https://hackernoon.com/images/471bw32gl.jpg)

## what is Linked Lists:
A linked list is a sequence of data elements, which are connected together via links. Each data element contains a connection to another data element in form of a pointer

### types of Linked List:
1. Singly : Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

2. Doubly : Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

![](https://i.pinimg.com/600x315/90/91/6d/90916d16e1c90dd0b56e9034239d08e0.jpg)


## whta is Node? 
Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.


### Next
 - Each node contains a property called Next. This property contains the reference to the next node.

### Head 
- The Head is a reference type of type Node to the first node in a linked list.

### Current
 - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.


 ##  traverse through a linked list :

- Current: is node that will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.
- When constructing your code, a few things to keep in mind :

- When making your Node class, consider requiring a value to be passed in to require that each node has a value.

- When making a Linked List, you may want to require that at least one node gets passed in upon instantiation. This first node is what your Head and Current will point too.

## linear data structures:
 which means that there is a sequence and an order to how they are constructed and traversed.

## non-linear data structures:
 items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.

## Big O Notation
is a way of evaluating the performance of an algorithm. takes into account the speed and efficiency with which something functions when its input grows to be any (crazy big!) size.

![](https://miro.medium.com/max/1152/1*MojRMNBNOHLqwe5ak7hTug.png)




### O:
 referred to as just “O” or sometimes as “order”, and a variable n, where n is the size of the input

### O(1):
 function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm.

### O(n):
 function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.

### O(n²):
 function : which clearly takes exponentially more time and memory the more elements that you have. It’s pretty safe to say that we want to avoid O(n²) algorithms, just from looking at that crazy red line!