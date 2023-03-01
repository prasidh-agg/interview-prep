# ☕️ Java basic concepts ☕️

This is a collection of common Java interview questions and their corresponding answers. The questions are organized by topic, including OOPs concepts, data structures, exception handling, and multithreading.

## ☕️ OOPs

### 1. What are the 4 OOPs concepts in Java?

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

***

## ☕️ Data Structures

### What is an ArrayList in Java?

An ArrayList in Java is a dynamic array that allows for the insertion and deletion of elements. It provides the following features:

- Resizable array implementation
- Provides constant-time positional access
- Allows for adding or removing elements at any position

### What is a LinkedList in Java?

A LinkedList in Java is a data structure that consists of a sequence of nodes, each containing a reference to the next node in the sequence. It provides the following features:

- Elements are stored as separate objects
- Provides constant-time positional access
- Allows for adding or removing elements at any position

### What is a HashMap in Java?

A HashMap in Java is a map of key-value pairs. It provides the following features:

- Uses hash table implementation for storing and retrieving entries
- Provides constant-time performance for most operations, including adding, removing, and retrieving entries
- Does not allow duplicate keys

***

## ☕️ Exception Handling

### What is the difference between checked and unchecked exceptions in Java?

Checked exceptions are checked at compile-time and are required to be handled by the calling code. Examples of checked exceptions include IOException and SQLException. Unchecked exceptions are not checked at compile-time and do not need to be handled by the calling code. Examples of unchecked exceptions include NullPointerException and ArrayIndexOutOfBoundsException.

### What is the purpose of try-catch blocks in Java?

Try-catch blocks in Java are used for exception handling. They allow developers to catch and handle exceptions that may be thrown by their code, preventing the code from crashing or producing unexpected results.

***

## ☕️ Multi-threading

### What is multithreading in Java?

Multithreading in Java is the ability of a program to execute multiple threads concurrently. Each thread runs independently of the others, allowing for more efficient use of system resources.

### What is the difference between a process and a thread in Java?

A process is a self-contained execution environment that runs independently of other processes. A thread is a lightweight sub-process that can run concurrently with other threads within a process.

### What is synchronization in Java?

Synchronization in Java is the process of controlling access to shared resources by multiple threads. It is used to prevent race conditions and ensure that only one thread at a time can access a shared resource.

***

## ☕️ SOLID Principles in Java

The SOLID principles are a set of design principles that were introduced by Robert C. Martin to help developers build better software that is easy to maintain, extend, and refactor. These principles are widely used in Java programming, and they aim to improve the quality of software by making it more flexible, robust, and scalable. In this answer, we will explain each of the SOLID principles and provide code examples to illustrate how they can be implemented in Java.

### S - Single Responsibility Principle (SRP)

- The Single Responsibility Principle states that a class should have only one reason to change. In other words, a class should have only one responsibility or function. This principle helps to create more maintainable and extensible code, as classes with a single responsibility are easier to test, maintain, and modify.

- To implement the SRP, we can create separate classes for each responsibility or function. For example, consider a class that manages a customer's order history and also handles payment processing. This violates the SRP as it has two responsibilities - managing order history and processing payments. We can split this class into two separate classes - one to manage the order history and another to handle payment processing.

```java
OrderHistory class with single responsibility
class OrderHistory {
    public void addOrder(Order order) {
        // add order to the order history
    }
    public List<Order> getOrderHistory() {
        // get the order history
    }
}
```

```java
// PaymentProcessor class with single responsibility
class PaymentProcessor {
    public void processPayment(Payment payment) {
        // process payment
    }
}
```

### O - Open-Closed Principle (OCP)

- The Open-Closed Principle states that software entities (classes, modules, functions, etc.) should be open for extension but closed for modification. This means that we should be able to extend the behavior of a class without modifying its source code. This principle helps to create more maintainable and reusable code, as changes to a class's behavior can be made without affecting its existing clients.

- To implement the OCP, we can use interfaces and abstract classes to define the behavior of a class, and then create concrete classes that implement or extend the interface or abstract class. For example, consider a class that calculates the price of a product based on its type. We can define an interface for the product type and create concrete classes that implement the interface. This way, we can add new product types without modifying the existing code.

```java
// ProductType interface
interface ProductType {
    public double calculatePrice(double basePrice);
}
```

```java
// Concrete classes that implement the ProductType interface
class BookType implements ProductType {
    public double calculatePrice(double basePrice) {
        // calculate price of book type
    }
}

class ElectronicType implements ProductType {
    public double calculatePrice(double basePrice) {
        // calculate price of electronic type
    }
}
```

```java
// Product class that uses the ProductType interface
class Product {
    private ProductType productType;

    public Product(ProductType productType) {
        this.productType = productType;
    }

    public double getPrice(double basePrice) {
        return productType.calculatePrice(basePrice);
    }
}
```

### L - Liskov Substitution Principle (LSP)

- The Liskov Substitution Principle states that objects of a superclass should be replaceable with objects of its subclass without affecting the correctness of the program. In other words, a subclass should be able to replace its superclass without changing the behavior of the program. This principle helps to create more robust and scalable code, as subclasses can be added or removed without affecting the existing code.

- To implement the LSP, we should ensure that subclasses follow the same contract as their superclass. This means that they should implement the same methods and have the same behavior as the superclass. For example, consider a class hierarchy for shapes. We can define a Shape superclass and create subclasses for specific shapes like Rectangle and Circle. The LSP requires that any method that works with a Shape object should also work with a Rectangle or Circle object.

```java
// Shape superclass
abstract class Shape {
    public abstract double getArea();
}
```

```java
// Rectangle subclass
class Rectangle extends Shape {
    private double length;
    private double width;

    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }

    public double getArea() {
        return length * width;
    }
}
```

```java
// Circle subclass
class Circle extends Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    public double getArea() {
        return Math.PI * radius * radius;
    }
}

// ShapeCalculator class that works with Shape objects
class ShapeCalculator {
    public double sumAreas(Shape[] shapes) {
        double sum = 0.0;
        for (Shape shape : shapes) {
            sum += shape.getArea();
        }
        return sum;
    }
}
```

### I - Interface Segregation Principle (ISP)

- The Interface Segregation Principle states that a client should not be forced to depend on methods it does not use. In other words, we should not create interfaces that have too many methods that are not relevant to all clients. This principle helps to create more maintainable and flexible code, as interfaces can be designed specifically for each client.

- To implement the ISP, we should create interfaces that have only the methods that are relevant to each client. For example, consider a printer interface that has methods for printing, scanning, and copying. If a client only needs to print, we should create a separate printing interface that has only the print method.

```java
// Printer interface with too many methods
interface Printer {
    public void print();
    public void scan();
    public void copy();
}
```

```java
// Printing interface with only the print method
interface Printing {
    public void print();
}
```

```java
// PrinterClient class that depends on the Printing interface
class PrinterClient {
    private Printing printer;

    public PrinterClient(Printing printer) {
        this.printer = printer;
    }

    public void printDocument(Document doc) {
        printer.print(doc);
    }
}
```

### D - Dependency Inversion Principle (DIP)

- The Dependency Inversion Principle states that high-level modules should not depend on low-level modules. Instead, both should depend on abstractions. This means that we should depend on interfaces and abstract classes rather than concrete implementations. This principle helps to create more flexible and reusable code, as changes to low-level modules do not affect the high-level modules.

- To implement the DIP, we should use interfaces and abstract classes to define the behavior of a module, and then create concrete classes that implement or extend the interface or abstract class. For example, consider a class that sends notifications to users. We can define an interface for the notification system and create concrete classes that implement the interface. This way, we can easily switch between different notification systems without modifying the existing code.

```java
// NotificationSystem interface
interface NotificationSystem {
    public void sendNotification(String message);
}
```

```java
// EmailNotificationSystem class that implements the NotificationSystem interface
class EmailNotificationSystem implements NotificationSystem {
    public void sendNotification(String message) {
        // send email notification
    }
}

// SMSNotificationSystem class that implements the NotificationSystem interface
class SMSNotificationSystem implements NotificationSystem {
    public void sendNotification(String message) {
        // send SMS notification
    }
}
```

```java
// NotificationService class that uses the NotificationSystem interface and depends on abstractions rather than concrete implementations
class NotificationService {
private NotificationSystem notificationSystem;


public NotificationService(NotificationSystem notificationSystem) {
    this.notificationSystem = notificationSystem;
}

public void sendNotification(String message) {
    notificationSystem.sendNotification(message);
}
}
```
