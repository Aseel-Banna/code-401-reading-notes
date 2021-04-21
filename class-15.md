# Trees 
A tree has these components:
* Node - A Tree node is a component which may contain it’s own values, and references to other nodes
* Root - The root is the node at the beginning of the tree
* K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
* Left - A reference to one child node, in a binary tree
* Right - A reference to the other child node, in a binary tree
* Edge - The edge in a tree is the link between a parent and child node
* Leaf - A leaf is a node that does not have any children
* Height - The height of a tree is the number of edges from the root to the furthest leaf

* Traversing a tree allows us to search for a node.
* There are two categories of traversals when it comes to trees:
  * Depth First:  is where we prioritize going through the depth (height) of the tree first.
     * Pre-order: root >> left >> right
     * In-order: left >> root >> right
     * Post-order: left >> right >> root
  * Breadth First: iterates through the tree by going through each level of the tree node-by-node. 


### Binary Tree Vs K-ary Trees
* Trees can have any number of children per node, but Binary Trees restrict the number of children to two.
* K-ary Trees:
  Traversing a K-ary tree requires a similar approach to the breadth first traversal.

### Big O
The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n).

### Binary Search Trees
A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.

### Big O
The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height).
