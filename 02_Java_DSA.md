# Basics of Java (by chatGPT)

## 1. What are data structures? Why are they important in programming?

- Data structures are a way of storing and organizing data in memory in a particular way. They enhance the basic operations of retrieving, storing, and modifying data, depending on different use cases.

## 2. What is the difference between an array and a linked list?

- An array stores data in contiguous memory locations and does not allow modifications, only allowing the same data type. A linked list stores data in non-contiguous memory locations, allowing for dynamic size. Array retrieval is fast O(1), but addition/deletion from the middle is expensive. In contrast, linked list traversal is expensive, but addition/deletion in the middle is faster than an array.

## 3. How would you implement a stack using a linked list?

- We need to maintain the head of the linked list, which serves as the top of the stack so that we can poll/peek it.
- We need to be able to push elements onto the stack, which means being able to create individual elements of the linked list.
- The push method adds an element to the linked list and makes it the new top of the stack.
- The pop method checks if the stack is not empty, then returns the top of the stack, which is the head of the linked list.
- The peek method just returns the value of the top of the stack.
- Answered by user with additional explanation by ChatGPT

## 4. What is a queue? How can it be implemented in Java?

- A queue is a first-in, first-out data structure that maintains the order in which elements arrive. It can be implemented using two stacks in Java or using the Queue class from the Collections utility. It can also be implemented using a doubly linked list.
  
## 5. What is a binary search tree?

- A binary search tree is a tree-like data structure in which each node has at most two children, and the elements in the subtree on the left are always smaller than the root node, while the elements in the subtree on the right are always bigger than the root node.

## 6. What is the difference between a stack and a queue?

- A stack is a last-in, first-out data structure, while a queue is a first-in, first-out data structure.

## 7. What is the difference between a heap and a binary search tree?

- A heap is a complete binary tree that satisfies the heap property, while a binary search tree is a binary tree in which each node has at most two children and follows a specific ordering property.

## 8. Can you show an example of a heap and a binary search tree? What are the differences between them?

- A heap example: [4, 10, 8, 14, 12, 20, 16]
- A binary search tree example:

```text
      10
     /  \
    6    14
   / \   / \
  4   8 12  16
```

- The main difference between a heap and a binary search tree is that a heap satisfies the heap property, which is that the parent node is
