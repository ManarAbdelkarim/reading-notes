# Implementation: Stacks and Queues

![](https://pbs.twimg.com/media/EoPCFBBVgAQHv2L.png:large)

## Stack:
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--s1Qbl8Gf--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/mwcwre09s12vqa3gvl7a.png)

### Common terminology for a stack is:
- Push - Nodes or items that are put into the stack are pushed
- Pop - Nodes or items that are removed from the stack are popped. When - you attempt to pop an empty stack an exception will be raised.
- Top - This is the top of the stack.
- Peek - When you peek you will view the value of the top Node in the - stack. When you attempt to peek an empty stack an exception will be raised.
- IsEmpty - returns true when stack is empty otherwise returns false.


## Stacks follow these concepts:

- FILO
(First In Last Out)

    This means that the first item added in the stack will be the last item popped out of the stack.

- LIFO
(Last In First Out)

    This means that the last item added to the stack will be the first item popped out of the stack.

### Big(O) for Stack Operations:

- Push O(1)
- pop O(1)
- Peek O(1)
- IsEmpty O(1)


### Stack Operations Algorithms:

- Push :

        ALOGORITHM push(value)
        // INPUT <-- value to add, wrapped in Node internally
        // OUTPUT <-- none
        node = new Node(value)
        node.next <-- Top
        top <-- Node

- Pop : 

        ALGORITHM pop()
        // INPUT <-- No input
        // OUTPUT <-- value of top Node in stack
        // EXCEPTION if stack is empty

        Node temp <-- top
        top <-- top.next
        temp.next <-- null
        return temp.value


- Peek : 

        ALGORITHM peek()
        // INPUT <-- none
        // OUTPUT <-- value of top Node in stack
        // EXCEPTION if stack is empty

        return top.value


- IsEmpty :

        ALGORITHM isEmpty()
        // INPUT <-- none
        // OUTPUT <-- boolean

        return top = NULL

## Queue

A Queue is a linear structure which follows a particular order in which the operations are performed. 

![](https://prepinsta.com/wp-content/uploads/2020/04/Queue-Data-Structures-1024x1024.png)



### Common terminology for a Queue is:
- Enqueue - Nodes or items that are added to the queue.
- Dequeue - Nodes or items that are removed from the queue. If called -  when the queue is empty an exception will be raised.
- Front - This is the front/first Node of the queue.
- Rear - This is the rear/last Node of the queue.

- Peek - When you peek you will view the value of the front Node in the - queue. If called when the queue is empty an exception will be raised.
- IsEmpty - returns true when queue is empty otherwise returns false.


## Queues follow these concepts:

- FIFO
(First In First Out)

    This means that the first item in the queue will be the first item out of the queue.


- LILO
(Last In Last Out)

    This means that the last item in the queue will be the last item out of the queue.

### Big(O) for Queue Operations:

- Enqueue O(1)
- Dequeue O(1)
- Peek O(1)
- IsEmpty O(1)


### Queue Operations Algorithms:

- Enqueue :

        ALGORITHM enqueue(value)
        // INPUT <-- value to add to queue (will be wrapped in Node internally)
        // OUTPUT <-- none
        node = new Node(value)
        rear.next <-- node
        rear <-- node

- Dequeue : 

        ALGORITHM dequeue()
        // INPUT <-- none
        // OUTPUT <-- value of the removed Node
        // EXCEPTION if queue is empty

        Node temp <-- front
        front <-- front.next
        temp.next <-- null

        return temp.value


- Peek : 

        ALGORITHM peek()
        // INPUT <-- none
        // OUTPUT <-- value of top Node in stack
        // EXCEPTION if stack is empty

        return front.value


- IsEmpty :

        ALGORITHM isEmpty()
        // INPUT <-- none
        // OUTPUT <-- boolean

        return front = NULL
