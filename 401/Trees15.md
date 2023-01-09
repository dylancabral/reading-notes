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

## Resources

[Trees Reading](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

## Things i want to know more about