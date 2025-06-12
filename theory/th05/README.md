# Queue in Java

## What is a Queue?

A **Queue** is a linear data structure that follows the **FIFO** rule: **First In, First Out**. The first element added to the queue will be the first one to be removed.

---

## Real-Life Analogy

Think of people standing in a line to buy movie tickets. The first person to join the line gets served first. This is exactly how a queue works.

---

## Basic Queue Operations

| Operation  | Description                                   |
| ---------- | --------------------------------------------- |
| `add()`    | Adds an element to the end (enqueue)          |
| `remove()` | Removes the front element (dequeue)           |
| `peek()`   | Returns the front element without removing it |

---

## Queue in Java using LinkedList

Java does not have a direct Queue class. Instead, it uses the `Queue` interface and classes like `LinkedList` to implement it.

### Step 1: Import Required Classes

```java
import java.util.Queue;
import java.util.LinkedList;
```

### Step 2: Create and Use a Queue

```java
Queue<String> line = new LinkedList<>();

line.add("Ali");
line.add("Sara");
line.add("Ahmed");

System.out.println("Front of the queue: " + line.peek());  // Ali

line.remove();  // Removes Ali

System.out.println("Front after removal: " + line.peek());  // Sara
```

---

## Full Example

```java
import java.util.Queue;
import java.util.LinkedList;

public class QueueExample {
    public static void main(String[] args) {
        Queue<String> students = new LinkedList<>();

        students.add("Ali");
        students.add("Sara");
        students.add("Ahmed");

        System.out.println("First in line: " + students.peek());

        students.remove();
        System.out.println("Now first in line: " + students.peek());
    }
}
```

### Output:

```
First in line: Ali
Now first in line: Sara
```

---

## Use Cases of Queue

* Printer Queue
* Customer Support Systems
* CPU Task Scheduling
* Breadth-First Search (BFS) in Trees and Graphs

---

## Limitations of Queue

* No random access like arrays or lists
* Can only remove from the front
* Can only insert at the rear

---

## Summary

* Queue = FIFO = First In, First Out
* Java uses `LinkedList` to implement Queue
* Use `add()`, `remove()`, and `peek()` methods
* Perfect for tasks that need to process items in order

---
