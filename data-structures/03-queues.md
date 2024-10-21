# Queues

- Contain data nodes
- Support three main operations:
    - Enqueue adds data to the back of the queue
    - Dequeue removes and provides data from the front of the queue
    - Peek provides data on the front of the queue
- Can be implemented using a linked list or array
- Bounded queues have a limited size.
- Enqueueing onto a full queue causes a queue overflow
    - Underflow occurs when we try to remove elements from an already empty queue – we cannot remove a node if it doesn’t exist. Underflow affects queues whether they are bounded or unbounded.
    - Overflow occurs when we add an element to a queue that does not have room for a new node.
- Queues process data First In, First Out (FIFO)
- Queues that restrict the number of elements they can store are called bounded queues.

<img src="./images/queues.png" />