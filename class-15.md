# Reading Notes 15  

Common Terminology
- `Node`: A node is the individual item/data that makes up the data structure.  
- `Root`: The root is the first/top `Node` in the tree.  
- `Left Child`: The node that is positioned to the left of a root or node.  
- `Right Child`: The node that is positioned ot the right of a root or node.  
- `Edge`: The edge in a tree is the link between a parent and child node.  
- `Leaf`: A leaf is a node that does not contain any children.  
- `Height`: The height of a tree is determined by the number of edges from the root to the bottom most node.  

Traversals  
- There are two categories of traversals when it comes to trees:  
    - Depth First: Priortizes going through the depth(height) of the tree first.  
        - Pre-order: `root >> left >> right`  
        - In-order: `left >> root >> right`  
        - Post-order: `left >> right >> root`  
    - Breadth First  
        - Iterates through the tree by going through each level of the tree node by node.  
        - Uses a queue instead of a call stack via recursion.  
- Most common way to traverse through a tree is to use recursion.  

Binary Trees  
- Trees can have any number o children per node, but Binary Trees restrict the number of children to two.  

Binary Search Trees  
- BST for short, is a type of tree that does have some structure attached to it.  
    - They are nodes organized in a manner where all values that are small than the `root` are placed to the left and all values that are larger than the `root` are placed to the right.  
- Best way to approach a BST is with a `while` loop.  
- BST insertion and search methods are O(h) or O(height) of the tree. You might have to search all the nodes down the a single leaf.  
- A balanced perfect BST is log(n).  
- Big space complexity of BST would be O(1). There is no allocating of additional space in order to work through the tree.  


## Additional Resources  
* [Read: Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)  