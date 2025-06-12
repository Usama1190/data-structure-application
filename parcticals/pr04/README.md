# Loops in Java: for, while, do-while

## Objective

Understand how to repeat code using different types of loops in Java:

* `for` loop
* `while` loop
* `do-while` loop

---

## Code Explanation

### ➞ Step 1: for Loop

```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Count: " + i);
}
```

* Starts a counter `i` at 1
* Runs the block as long as `i <= 5`
* Increases `i` by 1 in each iteration
* Prints: Count: 1, Count: 2, ..., Count: 5

### ➞ Step 2: while Loop

```java
int j = 1;
while (j <= 3) {
    System.out.println("While loop: " + j);
    j++;
}
```

* Starts with `j = 1`
* Checks condition before running
* Prints 3 times until `j` becomes 4

### ➞ Step 3: do-while Loop

```java
int k = 1;
do {
    System.out.println("Do-While: " + k);
    k++;
} while (k <= 2);
```

* Executes code **at least once** before checking condition
* Prints "Do-While: 1" and "Do-While: 2"

---

## Output

```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
While loop: 1
While loop: 2
While loop: 3
Do-While: 1
Do-While: 2
```

---

## Notes

* Use `for` loop when you know how many times to repeat.
* Use `while` or `do-while` when the end condition is based on logic.
* `do-while` always runs at least once.
