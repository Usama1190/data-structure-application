# Binary Search

## What You Will Learn

* What is Binary Search?
* When and why to use Binary Search
* How Binary Search works (step-by-step)
* How to implement Binary Search in Java
* Real-life example of Binary Search
* Comparison with Linear Search

---

## What is Binary Search?

**Binary Search** is a fast way to search for an element in a **sorted** array. Instead of checking each element one by one (like Linear Search), Binary Search repeatedly divides the array in half and checks where the target might be.

---

### Real-Life Example

> Imagine you're looking for a word in a dictionary.
> You don’t start at the first page — you open the middle and narrow down.
> That’s exactly how binary search works!

---

## When to Use Binary Search

* Use it when the array is **sorted**
* When you need **fast searching**
* Ideal for large data sets

---

## How Binary Search Works (Step-by-Step)

1. Start with the middle element of the array.
2. If the target is equal to the middle, return its index.
3. If the target is less than the middle, repeat the search in the **left half**.
4. If the target is greater than the middle, repeat the search in the **right half**.
5. Repeat until you find the element or the range becomes empty.

### Example:

Array: `[10, 20, 30, 40, 50, 60, 70]`
Target: `60`

Steps:

* Check middle → 40 → 60 is greater → search right half
* Check middle → 60 → match found!

---

## Java Code: Binary Search (Iterative)

```java
public class BinarySearchExample {
    public static int binarySearch(int[] arr, int target) {
        int start = 0;
        int end = arr.length - 1;

        while (start <= end) {
            int mid = (start + end) / 2;

            if (arr[mid] == target) {
                return mid; // target found
            } else if (arr[mid] < target) {
                start = mid + 1; // search right half
            } else {
                end = mid - 1; // search left half
            }
        }

        return -1; // not found
    }

    public static void main(String[] args) {
        int[] data = {10, 20, 30, 40, 50, 60, 70};
        int result = binarySearch(data, 60);
        
        if (result == -1) {
            System.out.println("Element not found.");
        } else {
            System.out.println("Element found at index: " + result);
        }
    }
}
```

---

## Comparison: Binary Search vs Linear Search

| Feature              | Binary Search     | Linear Search       |
| -------------------- | ----------------- | ------------------- |
| Array must be sorted | Yes               | No                  |
| Speed (Best case)    | Very Fast         | Slow                |
| Time Complexity      | O(log n)          | O(n)                |
| Use Case             | Large sorted data | Small/unsorted data |

---

## Summary

* Binary Search is **very efficient** but needs a **sorted array**.
* It divides the problem in half each time, making it super fast.
* Always check if the data is sorted before using it.

---
