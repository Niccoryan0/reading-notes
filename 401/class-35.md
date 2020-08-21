# 401-35 Readings

## Graphs
[Link](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)
- Graph terminology:
  - Vertex - Also called a node, vertexs are data objects that can have zero or more adjacent vertices.
  - Edge - Connection between two nodes
  - Neighbor - The neighbors of a node, nodes connected via an edge.
  - Degree - The degree of a certex is the number of connected edges.

- Undirected Graphs: Undirected or bidirectional, does not "flow" in one direction specfically.  A bidirectional graph example is shown below, image 1.

- Directed Graphs: In a directed graph (Digraph), every edge has a direction, usually denoted by arrows on the edge lines. Image 2 shows an example of this.

- Complete Graph: All nodes are connected to every other node. Image 3.

- Connected Graph: All nodes have at least one edge. Trees are a type of connected graph. Image 4.

- Disconnected Graph: Not all nodes have an edge. Image 5.

- Acyclic vs Cyclic:
  - Acyclic: Directed graph without cycles (when a node can be travered through and potentially end up back at itself). Also known as a DAG, trees are acyclic. Image 6.
  - Cyclic: Graph that has cycles, or a defined path of positive length that starts and ends at the same vertex. Image 7.

- Representing graphs:
  - Adjacency Matrix: 2d array, whos size is defined as n x n where n is the number of vertices. 0s and 1s are placed in each row of the array to represent where edges are between vertices. Image 8.
  - Adjacency List: Collection of linked lists or arrays that list all of other vertices connected to each vertice. They're straightforward and easy to view and understand. Image 9.

- Weighted Graph: Numbers are assigned to the edges, numbers called weights, and these numbers are then used when showing the Adjacency Matrix or List to specify the edge connections. Image 10.

### Traversals
- Breadth First: Using a queue, enqueue the declared start node, create a loop for running while the the node has nodes present, dequeue the first node from the queue and then if the Dequeued node has unvisited children, mark them as visited and res-insert them into the queue. Image 11.
```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    breadth.Enqueue(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                child.Visited <-- true
                breadth.Enqueue(child)   

    return nodes;
```
- Depth First: Use a stack, push the root node into it and run a while loop while stack is not empty, peek the top node and if it has unvisited children, mark it is visited and then push any unvisited children nodes into the stack, if no unvisited children pop that node off the stack, repeat until stack is empty. Example images can be found at: [Codefellows github](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)




## Images
### (1) Bidirectional Graph

![Bidirectional Graph image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

- Vertices/Nodes = {a,b,c,d,e,f}

- Edges = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}

### (2) Directed Graph (Digraph)

![Digraph image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

- Vertices = {a,b,c,d,e,f}

- Edges = {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}

### (3) Complete Graph

![Complete graph image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/CompleteGraph.PNG)

### (4) Connected Graph

![Connected graph image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/ConnectedGraph.PNG)

### (5) Disconnected Graph

![Disconnected graph image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DisconnectedGraph.PNG)

### (6) Acyclic Graphs

![Acyclic Graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/threeAcyclic.png)

### (7) Cyclic Graphs

![Cyclic Graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/cyclic.PNG)

### (8) Adjacency Matrix

![Adjacency matrix image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/AdjMatrix.PNG)

- Looking at the graph we are representing, you can see that Vertex A connects
to both Vertex D and Vertex C. To show this, we place a 1 in the position of (a,c) and (a,d).
- We follow this same pattern for the other vertex’s and where they are connected.
- If there is not an edge/connection between the vertex’s, we represent this by placing a 0 in the appropriate point of the matrix.

### (9) Adjacency List

![Adjacency list image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/AdjList.PNG)

- "Looking at the original graph that we are representing, we can see that Vertex A has an edge to both Vertex C and Vertex D. As a result, we will place both Vertex C and Vertex D in the adjacency list. Just from observation, we can see that we will only place the vertices that are connected in the list. If there is no connection between the vertices, they are not listed."

### (10) Weighted Graph

![Weighted graph image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightGraph.PNG)

How it's represented:

![Weight graph adjacency matrix](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightMatrix.PNG)

![Weight graph adjacency list](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/weightList.PNG)

### (11) Breadth First Traversal

![Breadth first traversal image](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/BreadthFirst.PNG)

