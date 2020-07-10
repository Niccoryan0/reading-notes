# 401-05 Readings

## Linked Lists
[Link](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

- Linked list: Data structure containing nodes that link/point to the next node in list.
- Singly: Number of references the node has, Single linked means only one reference to the Next and Previous node.
- Doubly: Two reference within the node to both Next and Previous nodes.
- Node: Individual items/links that live in a linked list, each contains data for a link.
- Next: Property of each node which references the next node.
- Head: Reference type of type Node to the first node in linked list
- Current: Reference type of type node to the currently viewed node. When traversing nodes, you typically reset the current to the head to gaurantee that you start from the beginning of the list.
- Linked lists cannot be iterated over with for and foreach loops, and we must use the Next value in each node to traverse them. A while loop allows continuous checking of the next node in the list.
- "Big O: The Big O of time for Includes would be O(n). This is because, at its worse case, the node we are looking for will be the very last node in the linked list. n represents the number of nodes in the linked list. The Big O of space for Includes would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input."
- Order of Operations is extremely important for working with Linked Lists, all reference to each link/node must be properly assigned.
- To set up a new node with O(1) efficiency: 
  1. Set Current equal to Head
  2. Instantiate the node using Add()
  3. newNode.Next is null by default, we want to set it to the same locaton that the Head node is pointing to. "Because Head is just a reference type, we will be assigning it to the same allocation in memory as the node it is pointing too. In this case, it’s Node1."
  4. Re-assign where Head is pointing, since Node1 is no longert the first node in the list, we re-assign Head to point to newNode
  5. "While we are at it, let’s just re-assign current as well to make sure should any further operation start at the new true start of the linked list."
- To set up a new node with O(n) efficiency (middle of the Singly Linked list): 
  1. Create a new node (node6) and set value to 16.
  2. Using AddBefore or AddAfter, insert the node into the list
- "The time efficiency of this transaction would be O(n) because we could be inserting the new node, worst case scenario, at the end. With n being the number of nodes possible, we would therefore have O(n) time efficiency. Space efficiency would stay at an O(1) because, like before, no additional space is being used allocated outside of what is given to us on the input"

## What’s a Linked List, Anyway pt1
[Link](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)
- Linked lists are linear data structures, meaning there is order and sequence to their construction and traversal.
- Linked lists don't need to take a single block of memory, they can be scattered throughout unlike arrays which require one chunk of memory to be set aside at their instantiation, arrays and static and linked lists are dynamic.
- Circular Linked Lists don't end with a node pointing to null value, they have nodes that act as tails rather than conventional head nodes, and the node after the tail is the beginning.

## What’s a Linked List, Anyway pt2
[Link](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)
- Linked lists primarily deal in O(1) and O(n) efficiency depending on what type of traversal is being done on the list.
- Linked lists don't need to initially declare memory allocation, rather they need to rearrange the pointers to add new data so that the new node is pointed to correctly.
- For singly linked lsits, insert a new element at the beginning is simple:
  1. First, we find the head node of the linked list.
  2. Next, we’ll make our new node, and set its pointer to the current first node of the list.
  3. Lastly, we rearrange our head node’s pointer to point at our new node.
- As long as the steps are followed in the correct order that is all that's needed, but if step 3 happens before step 2 it can create a mess.
- Inserting one at the end is a different story:
  1. Find the node we want to change the pointer of (in this case, the last node)
  2. Create the new node we want to insert and set its pointer (in this case, to null)
  3. Direct the preceding node’s pointer to our new node
- However, we will need to traverse the entire list to find the last node, which will take time directly proportional the length of the list, hence the O(n) efficiency.
- "a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element."
