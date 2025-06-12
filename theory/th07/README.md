# Merge Sort

## What is Merge Sort?

Merge Sort is a sorting algorithm based on the **Divide and Conquer** technique. It divides the input array into two halves, calls itself recursively to sort the two halves, and then merges the two sorted halves.

---

## Real Usage

Imagine sorting a large number of exam papers. Instead of sorting the whole stack at once, you split it into smaller groups, sort each one separately, and then combine them in order. Merge Sort works similarly.

---

## How Merge Sort Works

**Step-by-step Example:**

Suppose we want to sort the array:
`[38, 27, 43, 3, 9, 82, 10]`

### Step 1: Divide

Split the array into halves until each subarray contains a single element:

```
[38, 27, 43, 3, 9, 82, 10]
→ [38, 27, 43] and [3, 9, 82, 10]
→ [38], [27], [43], [3], [9], [82], [10]
```

### Step 2: Conquer (Sort + Merge)

Now merge them back in a sorted way:

```
[27, 38], [27, 38, 43], [3, 9], [3, 9, 10, 82]
→ [3, 9, 10, 27, 38, 43, 82]
```

---

## Java Implementation

```java
public class MergeSort {
    public static void mergeSort(int[] arr, int left, int right) {
        if (left < right) {
            int mid = (left + right) / 2;

            mergeSort(arr, left, mid);
            mergeSort(arr, mid + 1, right);

            merge(arr, left, mid, right);
        }
    }

    public static void merge(int[] arr, int left, int mid, int right) {
        int n1 = mid - left + 1;
        int n2 = right - mid;

        int[] L = new int[n1];
        int[] R = new int[n2];

        for (int i = 0; i < n1; i++)
            L[i] = arr[left + i];
        for (int j = 0; j < n2; j++)
            R[j] = arr[mid + 1 + j];

        int i = 0, j = 0, k = left;

        while (i < n1 && j < n2) {
            if (L[i] <= R[j]) {
                arr[k++] = L[i++];
            } else {
                arr[k++] = R[j++];
            }
        }

        while (i < n1) {
            arr[k++] = L[i++];
        }

        while (j < n2) {
            arr[k++] = R[j++];
        }
    }

    public static void main(String[] args) {
        int[] arr = {38, 27, 43, 3, 9, 82, 10};

        System.out.println("Before sorting:");
        for (int num : arr) {
            System.out.print(num + " ");
        }

        mergeSort(arr, 0, arr.length - 1);

        System.out.println("\nAfter sorting:");
        for (int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

## Time and Space Complexity

| Case    | Time Complexity |
| ------- | --------------- |
| Best    | O(n log n)      |
| Average | O(n log n)      |
| Worst   | O(n log n)      |

* **Space Complexity**: O(n) — because of temporary arrays used during merging.

---

## Comparison with Other Sorting Algorithms

| Algorithm      | Time Complexity | Space    | Stable |
| -------------- | --------------- | -------- | ------ |
| Bubble Sort    | O(n²)           | O(1)     | Yes    |
| Selection Sort | O(n²)           | O(1)     | No     |
| Merge Sort     | O(n log n)      | O(n)     | Yes    |
| Quick Sort     | O(n log n)      | O(log n) | No     |

---

## Summary

* Merge Sort uses Divide and Conquer.
* It is efficient and stable.
* Preferred for large data or external sorting.
* It needs extra space but gives consistent performance.
