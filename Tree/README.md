# Tree
It's one of the data structures that represent hierarchical data.

## Common Terminology
Some basic terms used in Tree data structure :
* Root: The root node is the topmost node in the tree hierarchy. In other words, the root node is the one that doesn't have any parent. In the above structure, node numbered 1 is the root node of the tree. If a node is directly linked to some other node, it would be called a parent-child relationship.
* Child node: If the node is a descendant of any node, then the node is known as a child node.
* Parent: If the node contains any sub-node, then that node is said to be the parent of that sub-node.
* Sibling: The nodes that have the same parent are known as siblings.
* Leaf Node:- The node of the tree, which doesn't have any child node, is called a leaf node. A leaf node is the bottom-most node of the tree. There can be any number of leaf nodes present in a general tree. Leaf nodes can also be called external nodes.
* Internal nodes: A node has atleast one child node known as an internal
* Ancestor node:- An ancestor of a node is any predecessor node on a path from the root to that node. The root node doesn't have any ancestors. In the tree shown in the above image, nodes 1, 2, and 5 are the ancestors of node 10.
* Descendant: The immediate successor of the given node is known as a descendant of a node. In the above figure, 10 is the descendant of node 5.

## Properties of Tree data structure

1. Recursive data structure: The tree is also known as a recursive data structure. A tree can be defined as recursively because the distinguished node in a tree data structure is known as a root node.

2. Number of edges: If there are n nodes, then there would n-1 edges. Each arrow in the structure represents the link or path. Each node, except the root node, will have atleast one incoming link known as an edge. There would be one link for the parent-child relationship.

3. Depth of node x: The depth of node x can be defined as the length of the path from the root to the node x. One edge contributes one-unit length in the path. So, the depth of node x can also be defined as the number of edges between the root node and the node x. The root node has 0 depth.

4. Height of node x: The height of node x can be defined as the longest path from the node x to the leaf node.

## Applications of trees
* Storing naturally hierarchical data: Trees are used to store the data in the hierarchical structure. For example, the file system. The file system stored on the disc drive, the file and folder are in the form of the naturally hierarchical data and stored in the form of trees.
* Organize data: It is used to organize data for efficient insertion, deletion and searching. For example, a binary tree has a logN time for searching an element.
* Trie: It is a special kind of tree that is used to store the dictionary. It is a fast and efficient way for dynamic spell checking.
* Heap: It is also a tree data structure implemented using arrays. It is used to implement priority queues.
* B-Tree and B+Tree: B-Tree and B+Tree are the tree data structures used to implement indexing in databases.
* Routing table: The tree data structure is also used to store the data in routing tables in the routers.

# Binary Search Tree 
A Binary Search Tree is a binary tree with search properties where elements in the left sub-tree are less than to the root and elements in the right sub-tree are greater than to the root.

## Searching an Element in a Binary Search Tree (BST)

To find an element in a Binary Search Tree, we first need to compare the element with the root node; if it matches then we have the right node otherwise we need to check the left or right.
```
public object SearchElement_Rec(objectelement, TNoderoot)

        {

           current = root;

            if (current == null)

                return "Not found";

            if (Convert.ToInt32(element)== Convert.ToInt32(current.Data))

                return element;

            if (Convert.ToInt32(element)< Convert.ToInt32(current.Data))          

                return this.SearchElement_Rec(element,current.Left);       

            else        

                return this.SearchElement_Rec(element,current.Right);                       

       }
```
## Representation
BST is a collection of nodes arranged in a way where they maintain BST properties. Each node has a key and an associated value. While searching, the desired key is compared to the keys in BST and if found, the associated value is retrieved.

## Basic Operations
**Search** − Searches an element in a tree.

**Insert** − Inserts an element in a tree.

**Pre-order** Traversal − Traverses a tree in a pre-order manner.

**In-order** Traversal − Traverses a tree in an in-order manner.

**Post-order** Traversal − Traverses a tree in a post-order manner.


***To learn more*** [Tree](https://www.javatpoint.com/tree).