# Reading Notes 35  

KEY NOTES:

### Graphs  
- A graph is a non-linear data structure that can be looked at as a collection of `vertices` (or `nodes`) potentially connected by line segments named `edges`.

### Directed vs Undirected  
- An `Undirected Graph` is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.
- A `Directed Graph` also called a Digraph is a graph where every edge is directed.

### Complete vs Connected vs Disconnected  
- Complete Graphs  
    - A complete graph is when all `nodes` are connected to all other `nodes`.  
- Connected Graph  
    - A connected graph is graph that has all of `vertices`/`nodes` have at least one `edge`.  
    - A `Tree` is a form of a connected graph.  
- Disconnected Graph  
    - A disconnected graph is a graph where some `vertices` may not have `edges`.

### Acyclic vs Cyclic  
- Acyclic Graph  
    - An acyclic graph is a directed graph without cycles.  
    - A cycle is when a `node` can be traversed through and potentially end up back at itself.
    - A directed acyclic graph is also called a `DAG`. This can also be represented as what we know as a `tree`.
- Cyclic Graph  
    - A Cyclic graph is a graph that has cycles.  
    - A cycle is defined as a path of a positive length that starts and ends at the same vertex.  

### Graph Representation  
- Adjacency Matrix  
    - An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix  
- Adjacency List  
    - An adjacency list is the most common way to represent graphs. An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.  

### Weighted Graphs  
- A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.  

### Traversals  
- You will be required to traverse through a graph. The traversals itself are like those of trees.  
    - Breadth First  
    - Depth First  

### Real World uses of Graphs  
- GPS and Mapping 
- Driving Directions  
- Social Networks  
- Airline Traffic  
- Netflix uses graphs for suggestions of products  


## Addtional Resources  
* [Read: Graphs](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)  