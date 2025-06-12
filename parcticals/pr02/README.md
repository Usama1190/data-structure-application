# Practical 02: Arrays in Java

This practical demonstrates how to declare, initialize, and use arrays in Java, based on **Topic 02: Arrays**.

---

## 🔸 Objective

- Understand what an array is.
- Learn how to declare, create, and initialize arrays in Java.
- Access array elements.
- Loop through arrays using `for` and `for-each` loops.

---

## 🧠 Concepts Covered

- Fixed-size containers to hold elements of the same type.
- Index-based access.
- Looping through array elements.

---

## 📂 Files

- `main.java` → contains Java code for practicing arrays.

---

## 🧪 Steps Explained

### ✅ Step 1: Declare and Initialize an Array

```java
int[] numbers = {10, 20, 30, 40, 50};
This creates an array named numbers that stores 5 integers.

✅ Step 2: Access Elements by Index
java
Copy
Edit
System.out.println(numbers[0]);  // Output: 10
System.out.println(numbers[1]);  // Output: 20
Arrays in Java are zero-indexed, so numbers[0] gives the first item.

✅ Step 3: Loop Through Array Using for
java
Copy
Edit
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
This prints all elements from the numbers array using traditional indexing.

✅ Step 4: Loop Using for-each
java
Copy
Edit
for (int num : numbers) {
    System.out.println(num);
}
A shorter and cleaner way to iterate over all items in the array.

📌 Notes
Arrays are fixed in size.

All elements must be of the same data type.

We'll later learn more flexible structures like ArrayList.

✅ Output (Example)
Copy
Edit
10
20
30
40
50
