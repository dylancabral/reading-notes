# Trees Reading 

## Common terminology When workign with trees

* Node - A Tree node is a component which may contain its own values, and references to other nodes
* Root - The root is the node at the beginning of the tree
* K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
* Left - A reference to one child node, in a binary tree
* Right - A reference to the other child node, in a binary tree
* Edge - The edge in a tree is the link between a parent and child node
* Leaf - A leaf is a node that does not have any children
* Height - The height of a tree is the number of edges from the root to the furthest leaf

## Traversing a Binary tree

There is two types of binary tree traversal 
### Depth First

prioritize going through the depth or height of the tree first 
there are three ways to traverse when using depth first

> The most common way to traverse through a tree is to use recursion. With these traversals, we rely on the call stack to navigate back up the tree when we have reached the end of a sub-path.

### Pre-order root, left , right 

* pre-order meant that the root has to be looked at first if the value is not Null it will move to the left branch, if it is null the root will be added to the call stack
* this will find root nodes recursively until it finds a leaf node then it knows its hit the bottom of the tree 
 > The program will look for both a root.left and a root.right. Both will return null, so it will end the execution of that method call
D will pop off of the call stack and the root will be reassigned back to B
This is the heart of recursion: when we complete a function call, we pop it off the stack and are able to continue execution through the previous function call
 
pre order psudeo code
```python
# ALGORITHM preOrder(root)
# // INPUT <-- root node
# // OUTPUT <-- pre-order output of tree node's values
# 
#     OUTPUT <-- root.value
# 
#     if root.left is not Null
#         preOrder(root.left)
# 
#     if root.right is not NULL
#         preOrder(root.right)
```

### In-order left, root, right

in order Psuedo Code

```python
# ALGORITHM inOrder(root)
# // INPUT <-- root node
# // OUTPUT <-- in-order output of tree node's values
# 
#     if root.left is not NULL
#         inOrder(root.left)
# 
#     OUTPUT <-- root.value
# 
#     if root.right is not NULL
#         inOrder(root.right)
```


### Post-order left,right root

post order Psuedo Code

```python
# ALGORITHM postOrder(root)
# // INPUT <-- root node
# // OUTPUT <-- post-order output of tree node's values
# 
#     if root.left is not NULL
#         postOrder(root.left)
# 
#     if root.right is not NULL
#         postOrder(root.right)
# 
#     OUTPUT <-- root.value
```
The biggest difference between each of the traversals is when you are looking at the root node.

## Breadth First
>Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

Traditionally, breadth first traversal uses a queue (instead of the call stack via recursion) to traverse the width/breadth of the tree

### breadth first traversal code

```python
# ALGORITHM breadthFirst(root)
# // INPUT  <-- root node
# // OUTPUT <-- front node of queue to console
# 
#   Queue breadth <-- new Queue()
#   breadth.enqueue(root)
# 
#   while ! breadth.is_empty()
#     node front = breadth.dequeue()
#     OUTPUT <-- front.value
# 
#     if front.left is not NULL
#       breadth.enqueue(front.left)
# 
#     if front.right is not NULL
#       breadth.enqueue(front.right)
```
## K-ary Trees

If Nodes are able have more than 2 child nodes in the tree, we call the tree that contains them a K-ary Tree. Unlike Binary which refers to a maximum of 2

![Binary Tree](/images/BinaryTrees.png)

Traversing a K-ary tree requires a similar approach to the breadth first traversal. We are still pushing nodes into a queue, but we are now moving down a list of children of length k, instead of checking for the presence of a left and a right child.

## Psuedo Code for K-th Tree traversal Breadth FIrst

```python
# ALGORITHM breadthFirst(root)
# // INPUT  <-- root node
# // OUTPUT <-- front node of queue to console
# 
#   Queue breadth <-- new Queue()
#   breadth.enqueue(root)
# 
#   while ! breadth.is_empty()
#     node front = breadth.dequeue()
#     OUTPUT <-- front.value
# 
#     for child in front.children
#         breadth.enqueue(child)
```

## Adding a node in A Binary Tree

Adding a node
Because there are no structural rules for where nodes are “supposed to go” in a binary tree, it really doesn’t matter where a new node gets placed.

One strategy for adding a new node to a binary tree is to fill all “child” spots from the top down. To do so, we would leverage the use of breadth first traversal. During the traversal, we find the first node that does not have all its children filled, and insert the new node as a child. We fill the child slots from left to right.

In the event you would like to have a node placed in a specific location, you need to reference both the new node to create, and the parent node which the child is attached to.

## Big O For Binary Trees 

>The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.

    The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree.

    A “perfect” binary tree is one where every non-leaf node has exactly two children. The maximum width for a perfect binary tree, is 2^(h-1), where h is the height of the tree. Height can be calculated as log n, where n is the number of nodes

## Binary Search Tree

BST's are a Type of tree that does have structure unlike a Regluar BS a node will fit the first place it finds space, in a node where all its children are not filled. in a  BST the values less than the root will be aligned to the left and the values greater will be to the right of the root

![Binary Search Tree Format](/images/BST.png)

> Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

The best way to approach searching a bst is to use a while loop we cycle the loop until we hit a leaf or until we reach a match to the value we are searching for 

## Big O of a BST

> Big O
The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.
> 
    The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.

## Resources

[Trees Reading](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

## Things i want to know more about

This was a every detailed reading, i hope that soon the psuedo code makes more sense in the translation to actual runnable code but I am happy with the reading, i need more time to practice 