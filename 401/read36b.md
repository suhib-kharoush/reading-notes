# Graphs

- A graph is a non-linear data structure that can be looked at as a collection of `vertices` (or `nodes`) potentially connected by line segments named `edges`.

- Here is some common terminology used when working with Graphs:
- - Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
- - Edge - An edge is a connection between two nodes.
- - Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
- - Degree - The degree of a vertex is the number of edges connected to that vertex.

#### Directed vs Undirected

1. Undirected Graphs:
- An `Undirected Graph` is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

- For example, in the graph below, Node `C` is connected to `Node A`, `Node E` and `Node B`. There are no “directions” given to point to specific vertices. The connection is bi-directional.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/UndirectedGraph.PNG)

- - The undirected graph we are looking at has 6 vertices and 7 undirected edges.

- - Vertices/Nodes = {a,b,c,d,e,f}

- - Edges = {(a,c),(a,d),(b,c),(b,f),(c,e),(d,e),(e,f)}

2. Directed Graphs (Digraph):
- A `Directed Graph` also called a `Digraph` is a graph where every edge is directed.

- Unlike an undirected graph, a `Digraph` has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

- Compare the visual below with the undirected graph above. Can you see the difference? The `Digraph` has arrows pointing to specific nodes.
![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DirectedGraph.PNG)

- - The directed graph above has six vertices and eight directed edges

- - Vertices = {a,b,c,d,e,f}

- - Edges = {(a,c),(b,c),(b,f),(c,e),(d,a),(d,e)(e,c)(e,f)}


#### Complete vs Connected vs Disconnected:

- Complete Graphs
- A complete graph is when all nodes are connected to all other nodes.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/CompleteGraph.PNG)

1. Connected
- A connected graph is graph that has all of vertices/nodes have at least one edge.


![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/ConnectedGraph.PNG)


2. Disconnected
- A disconnected graph is a graph where some vertices may not have edges.

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/DisconnectedGraph.PNG)

#### Acyclic vs Cyclic
- In addition to undirected and directed graphs, we also have acyclic and cyclic graphs.

1. Acyclic Graph
- An acyclic graph is a directed graph without cycles.

- A cycle is when a node can be traversed through and potentially end up back at itself.

2. Cyclic Graphs
- A Cyclic graph is a graph that has cycles.

- A cycle is defined as a path of a positive length that starts and ends at the same vertex.

#### Graph Representation
-We represent graphs through:

- - Adjacency Matrix
- - Adjacency List

#### Adjacency Matrix
- An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix

#### Adjacency List
- An adjacency list is the most common way to represent graphs.

- An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

- Adjacency lists make it easy to view if one vertices connects to another.

- This is what an Adjacency List looks like:

![](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/assets/AdjList.PNG)
