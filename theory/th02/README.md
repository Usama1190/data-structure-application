# Arrays

---

## What You Will Learn

* What is an Array?
* Why do we need Arrays?
* How to create and use Arrays in Java
* Real-life example of Arrays
* Looping through Arrays
* Limitations of Arrays

---

## What is an Array?

An **Array** is like a *box* that holds a fixed number of values — all of the same type (like all integers or all names).

Think of it like this:

> Imagine an egg carton.
> It has 12 fixed spaces and each space holds 1 egg.
> That’s how an array works — fixed size, same type.

---

## Why Use Arrays?

Without arrays:

```java
int num1 = 10;
int num2 = 20;
int num3 = 30;
// and so on...
```

With arrays:

```java
int[] numbers = {10, 20, 30};
```

**Benefits:**

* Group multiple values together
* Easier to loop through
* Saves time and lines of code

---

## How to Declare and Use Arrays in Java

### Step 1: Declare the array

```java
int[] numbers;
```

### Step 2: Create (allocate) the array

```java
numbers = new int[5];  // creates space for 5 integers
```

### Step 3: Add values

```java
numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;
```

Or do it all at once:

```java
int[] numbers = {10, 20, 30, 40, 50};
```

---

## Real-Life Example

> Think of your school timetable.
> Each day has 5 periods: English, Math, Science, etc.

```java
String[] subjects = {"English", "Math", "Science", "Computer", "Urdu"};
```

---

## Looping Through Arrays

To go through each item in an array, we use a **loop**.

### Using `for` loop:

```java
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
```

### Using `for-each` loop (shorter way):

```java
for (int num : numbers) {
    System.out.println(num);
}
```

---

## Limitation of Arrays

* Fixed size — you can’t add or remove items after creation
* All items must be of the same data type

> For flexible data handling, we use `ArrayList` later on.

---

## Summary

* Arrays are containers that hold multiple values of the same type.
* They're useful when you want to store lots of related items.
* Java arrays are powerful, but limited in flexibility — we’ll learn better options soon!

---
