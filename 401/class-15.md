# 401-15 Readings

## Trees
### Terminology:
- Node
- Root (Front/Top)
- Left Child
- Right Child
- Edge (Link between parent and child nodes)
- Leaf (Node w/o children)
- Height (# of edges from root to bottommost node)
![Tree diagram](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)

### Traversals
#### Depth first
- Going through depth of tree is prioritized three methods described below:
- Depth first traversal is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the root. Here are three methods for depth first traversal:
  - Pre-order: root >> left >> right
  - In-order: left >> root >> right
  - Post-order: left >> right >> root

- Recursion is usually used to traverse through a tree
    PreOrder:
    ALGORITHM preOrder(root)

    OUTPUT <-- root.value

    if root.left is not NULL
      preOrder(root.left)

    if root.right is not NULL
      preOrder(root.right)

    InOrder:
    ALGORITHM inOrder(root)
    // INPUT <-- root node
    // OUTPUT <-- in-order output of tree node's values

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)

    PostOrder:
    ALGORITHM postOrder(root)
    // INPUT <-- root node
    // OUTPUT <-- post-order output of tree node's values

    if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value

- Preorder Recursion will move down the leftmost line of the tree until it pops a leaf node, then it will move back up one level and check again for a right node and continue moving down and then up until it has traversed the whole tree.

#### Breadth First
- Goes through each level of the tree node by node, popping off the very top node and enqueing it's children. It's children undergo the same process, so the approach starts popping from the top instead of going to the bottom and back up. 
  - PseudoCode
    ALGORITHM breadthFirst(root)
    // INPUT  <-- root node
    // OUTPUT <-- front node of queue to console

    Queue breadth <-- new Queue()
    breadth.enqueue(root)

    while breadth.peek()
      node front = breadth.dequeue()
      OUTPUT <-- front.value

      if front.left is not NULL
        breadth.enqueue(front.left)

      if front.right is not NULL
        breadth.enqueue(front.right)

### General
- Big O for inserting a new node and searching for a specific node are both O(n) for time time complexity. Breadth first the Big O would be O(w) where w is the largest width of the tree.
- Binary trees mean that each node can have two children, they are unordered by Binary Search trees place the nodes with lower value than the root to the left and higher values to the right. These have insert and search time complexity of O(h) where h is the height of the tree, in a perfect binary search tree this would be log(n).