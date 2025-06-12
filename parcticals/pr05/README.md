# Topic 5 – Java Conditional Statements

## Objective

Learn how to use conditional statements in Java:

* `if`
* `else if`
* `else`
* Comparison and logical operators

---

## 🧪 Code Explanation

### ➞ Step 1: main Method

```java
public static void main(String[] args) {
    int age = 18;
    
    if (age < 13) {
        System.out.println("You are a child.");
    } else if (age < 20) {
        System.out.println("You are a teenager.");
    } else {
        System.out.println("You are an adult.");
    }
}
```

### ➞ Step 2: `if-else` Logic

* `if (age < 13)` → checks if the age is less than 13
* `else if (age < 20)` → runs if the age is between 13 and 19
* `else` → runs when none of the above conditions are true

---

## ✅ Output

```
You are a teenager.
```

---

## 📘 Notes

* Use `==` to compare equality (e.g., `if (a == b)`)
* Use `!=` for not equal
* Use `&&` (AND), `||` (OR) for combining conditions
* Always use curly braces `{}` to avoid mistakes and improve readability

---

## 🔄 Real-World Example

Conditional statements are used everywhere — for example:

* Showing age-specific content on a website
* Controlling access to features based on user role or status

---
