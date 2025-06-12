# Doubly Linked List in Java

## What You Will Learn

* What is a Doubly Linked List?
* How it is different from a Single Linked List
* Real-life examples and uses
* How to create and use a Doubly Linked List in Java
* Insertion (at start, end, and middle)
* Deletion (from start, end, and middle)
* Traversing in both directions

## What is a Doubly Linked List?

A **Doubly Linked List (DLL)** is a type of data structure that connects elements (called nodes) in both directions — forward and backward.

Each **node** contains:

* Data (like a number or word)
* A link to the **next** node
* A link to the **previous** node

```
null ← [data | prev | next] ⇄ [data | prev | next] ⇄ [data | prev | next] → null
```

## Real-Life Example

Imagine you're in a **photo gallery** app:

* You swipe **forward** to go to the next photo.
* You swipe **backward** to go to the previous one.

That’s how a Doubly Linked List works. You can move in both directions!

## Doubly Linked List vs Singly Linked List

| Feature                | Singly Linked List | Doubly Linked List  |
| ---------------------- | ------------------ | ------------------- |
| Navigation             | One-way            | Two-way             |
| Extra memory required  | Less               | More (prev pointer) |
| Ease of deleting nodes | Harder             | Easier              |
| Flexibility            | Less               | More                |

## Why Use Doubly Linked List?

* It allows traversal in **both directions**
* **Deleting** a node is easier because you have a previous pointer
* Useful for **undo-redo**, **browsers**, **navigation systems**

## How to Create a Doubly Linked List in Java

### Step 1: Define a Node

```java
class Node {
    int data;
    Node prev;
    Node next;

    Node(int data) {
        this.data = data;
    }
}
```

### Step 2: Create the DLL

```java
class DoublyLinkedList {
    Node head;
    Node tail;

    // Add node at end
    void addLast(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = tail = newNode;
        } else {
            tail.next = newNode;
            newNode.prev = tail;
            tail = newNode;
        }
    }
}
```

## Insert Elements

### At the Start

```java
void addFirst(int data) {
    Node newNode = new Node(data);
    if (head == null) {
        head = tail = newNode;
    } else {
        newNode.next = head;
        head.prev = newNode;
        head = newNode;
    }
}
```

### At the End

Already shown in `addLast()` above.

## Delete Elements

### From the Start

```java
void removeFirst() {
    if (head == null) return;

    if (head == tail) {
        head = tail = null;
    } else {
        head = head.next;
        head.prev = null;
    }
}
```

### From the End

```java
void removeLast() {
    if (tail == null) return;

    if (head == tail) {
        head = tail = null;
    } else {
        tail = tail.prev;
        tail.next = null;
    }
}
```

## Traverse the List

### Forward Traversal

```java
void printForward() {
    Node current = head;
    while (current != null) {
        System.out.print(current.data + " ");
        current = current.next;
    }
}
```

### Backward Traversal

```java
void printBackward() {
    Node current = tail;
    while (current != null) {
        System.out.print(current.data + " ");
        current = current.prev;
    }
}
```

## Summary

* Doubly Linked Lists can move **forward and backward**
* They're useful in apps like browsers, galleries, and undo systems
* Each node has data, a **next**, and a **previous** pointer
* Insertion and deletion become easier than singly linked lists
