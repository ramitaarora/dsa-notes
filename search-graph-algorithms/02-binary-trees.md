# Binary Trees

- A binary tree is an efficient data structure for fast data storage and retrieval due to its O(log N) runtime. 
- It is a specialized tree data structure that is made up of a root node, and at most two child branches or subtrees. 
- Each child node is itself a binary tree.
- Each node has the following properties:
    - data
    - a depth value, where depth of 1 indicates the top level of the tree and a depth greater than 1 is a level somewhere lower in the tree
    - a left pointer that points to a left child which is itself a binary tree, and must have a data lesser than the root node’s data
    - a right pointer that points to a right child which is itself a binary tree, and must have a data greater than the root node’s data

<img src="./images/binary-search-tree.svg" />

    If the new value is less than the root node's value
        If a left child node doesn't exist 
            Create a new BinaryTree with the new value at a greater depth and assign it to the left pointer
        Else
            Recursively call .insert() on the left child node  
    Else
        If a right child node doesn't exist
            Create a new BinaryTree with the new value at a greater depth and assign it to a right pointer
        Else
            Recursively call .insert() on the right child node

Recursive Method:

    If target value is the same as the current node value
        Return the current node
    Else
        If target value is less than the root node's value and there is a left child node
            Recursively search from the left child node
        Else if there is a right child node
            Recursively search from the right child node

### Traversing a Binary Tree

There are two main ways of traversing a binary tree: breadth-first and depth-first. 
- With breadth-first traversal, we begin traversing at the top of the tree’s root node, displaying its data and continuing the process with the left child node and the right child node. 
    - Descend a level and repeat this step until we finish displaying all the child nodes at the deepest level from left to right.
- With depth-first traversal, we always traverse down each left-side branch of a tree fully before proceeding down the right branch. However, there are three traversal options:
    - <i>Preorder</i> is when we perform an action on the current node first, followed by its left child node and its right child node
    - <i>Inorder</i> is when we perform an action on the left child node first, followed by the current node and the right child node
    - <i>Postorder</i> is when we perform an action on the left child node first, followed by the right child node and then the current node