# Java basic concepts

This is a collection of common Java interview questions and their corresponding answers. The questions are organized by topic, including OOPs concepts, data structures, exception handling, and multithreading.

## What are the 4 OOPs concepts in Java?

The four OOPs (Object-Oriented Programming) concepts in Java are:

1. Encapsulation
    - Keeps the code and data safe from external interference
    - Provides access to code and data through well-defined interfaces

2. Abstraction
    - Hides the implementation details of code and data
    - Provides a high-level view of the code and data

3. Inheritance
    - Enables code and data reuse
    - Provides a way to create new classes from existing ones

4. Polymorphism
    - Enables different objects to be treated as the same type
    - Provides a way to create code that can work with objects of different classes

## What is an ArrayList in Java?

An ArrayList in Java is a dynamic array that allows for the insertion and deletion of elements. It provides the following features:

- Resizable array implementation
- Provides constant-time positional access
- Allows for adding or removing elements at any position

## What is a LinkedList in Java?

A LinkedList in Java is a data structure that consists of a sequence of nodes, each containing a reference to the next node in the sequence. It provides the following features:

- Elements are stored as separate objects
- Provides constant-time positional access
- Allows for adding or removing elements at any position

## What is a HashMap in Java?

A HashMap in Java is a map of key-value pairs. It provides the following features:

- Uses hash table implementation for storing and retrieving entries
- Provides constant-time performance for most operations, including adding, removing, and retrieving entries
- Does not allow duplicate keys

## What is the difference between checked and unchecked exceptions in Java?

Checked exceptions are checked at compile-time and are required to be handled by the calling code. Examples of checked exceptions include IOException and SQLException. Unchecked exceptions are not checked at compile-time and do not need to be handled by the calling code. Examples of unchecked exceptions include NullPointerException and ArrayIndexOutOfBoundsException.

## What is the purpose of try-catch blocks in Java?

Try-catch blocks in Java are used for exception handling. They allow developers to catch and handle exceptions that may be thrown by their code, preventing the code from crashing or producing unexpected results.

## What is multithreading in Java?

Multithreading in Java is the ability of a program to execute multiple threads concurrently. Each thread runs independently of the others, allowing for more efficient use of system resources.

## What is the difference between a process and a thread in Java?

A process is a self-contained execution environment that runs independently of other processes. A thread is a lightweight sub-process that can run concurrently with other threads within a process.

## What is synchronization in Java?

Synchronization in Java is the process of controlling access to shared resources by multiple threads. It is used to prevent race conditions and ensure that only one thread at a time can access a shared resource.
