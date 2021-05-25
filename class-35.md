# Graph

* Graph is a collection of node that are related to each other by edges.
* The components of a graph:
  * Vertex (node)
  * Edges
  * Neighbor
  * Degree
* There are two types of graphs
  * According to the directions: 
    * Undirected: the edges are bi-directional
    * Directed (Digraph): edges are directed
  * According to connectivity:
    * Complete: all nodes are connected to all other nodes
    * Connected: all of nodes have at least one edge i.e ***trees***
    * Disconnected: some nodes have no edge
  * According to cycles:
    * Acyclic: directed without cycles (the node cannot return to itself)
    * Cyclic: the node can return to itself

* Graph Representation
1. Adjacency Matrix: if we have n nodes, we will have n x n boolean matrix, because it using 2D array. 
2. Adjacency List: a collection of linked lists or array that lists all of the other nodes are connected.

* Weighted Graphs: numbers assigned to edges. So, each edge has its weight, we can use weight matrix and weight list.
* Traversals
  * Breadth First: starting from one node and assign each visited node as visited to prevent the infinite loop of cyclic graph. It is using queue for nodes 
  * Depth First: same as breadth first, but here we use stack instead of queue.

* Real World Uses of Graphs
* GPS and Mapping
* Driving Directions
* Social Networks
* Airline Traffic
* Netflix uses graphs for suggestions of products

