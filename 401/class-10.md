# 401-10 Readings

## Stacks and Queues
[Link](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)
### Stack
- A stack is a data structure comprised of Nodes with references to the next node in the list.
- Common terminology for a stack is push, pop, top, peek and IsEmpty.
- FILO means the first added to the stack will be the last to pop out, and LIFO means the last item added will be the first to pop.
- Pushing a node is a O(1) operation because it always just adds a new node to the top.
- Pop is also O(1), typically preceded by checking if the Node IsEmpty to ensure an exception is not raised.
- Peek, also O(1), only inspects the top noce of the stack and is also usually preceded by checking is the node IsEmpty.
- IsEmpty is O(1) and checks if a Node is null.
![Stack visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/stack1.PNG)
### Queue
- Common terminology for a queue: enqueue, dequeue, front, rear, peek and IsEmpty.
- Stacks are FIFO and LILO, First in First Out and Last In Last Out, the opposite of stacks.
- Enqueue is O(1) and adds an item to the read of the queue.
- Dequeue is also O(1) and removes the front item in the queue.
- Front and Rear indicate positions in the queue, the first and last Nodes respectively.
- Peek and IsEmpty function the same but Peek checks the first item instead of the last.
![Queue visualization](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/images/Queue.PNG)