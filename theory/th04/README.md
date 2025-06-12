# Insertion Sort

## Content

* What is Insertion Sort?
* Why and where it is used
* Real-world analogy
* How it works step-by-step
* Java code example
* When to use it and when not to
* Summary

---

## What is Insertion Sort?

Insertion Sort is a simple sorting algorithm that builds the final sorted array one item at a time. It’s much like the way you might sort playing cards in your hand — pick a card and insert it into the correct position relative to the others.

---

## Why Use Insertion Sort?

* Easy to understand and implement
* Efficient for small datasets
* Performs well on nearly sorted data
* It sorts the array in-place (no extra memory)

---

## How Insertion Sort Works

1. Start from the second element.
2. Compare it with elements before it.
3. If smaller, shift the larger elements one position to the right.
4. Insert the element in its correct position.
5. Repeat for all elements.

### Example

Sort this array: `[5, 2, 4, 6, 1, 3]`

Step-by-step process:

```
Start at index 1 (2): Compare with 5 → Insert before → [2, 5, 4, 6, 1, 3]

Index 2 (4): Compare with 5 → Insert before 5 → [2, 4, 5, 6, 1, 3]

Index 3 (6): Already in correct position → [2, 4, 5, 6, 1, 3]

Index 4 (1): Move 6, 5, 4, 2 → Insert at beginning → [1, 2, 4, 5, 6, 3]

Index 5 (3): Move 4 and insert → [1, 2, 3, 4, 5, 6]
```

---

## Java Code Example

```java
public class InsertionSort {
    public static void main(String[] args) {
        int[] arr = {5, 2, 4, 6, 1, 3};

        for (int i = 1; i < arr.length; i++) {
            int key = arr[i];
            int j = i - 1;

            // Shift elements of arr[0..i-1], that are greater than key
            while (j >= 0 && arr[j] > key) {
                arr[j + 1] = arr[j];
                j--;
            }

            arr[j + 1] = key;
        }

        // Print sorted array
        for (int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

## Real-Life Analogy

Imagine sorting your test papers by marks manually — one by one, putting each paper in its correct spot relative to the others. That’s how insertion sort works.

---

## Time Complexity

| Case       | Time Complexity |
| ---------- | --------------- |
| Best Case  | O(n)            |
| Average    | O(n²)           |
| Worst Case | O(n²)           |

---

## When to Use

* When the dataset is small
* When the data is already nearly sorted
* For educational and learning purposes

## When Not to Use

* On large datasets
* When performance is a priority

---

## Summary

* Insertion sort is simple and works well on small or nearly sorted data.
* It is inefficient for large datasets.
* It’s a great starting point to understand how sorting algorithms work.
