# Java Basics: Hello World & Variables

## Objective

Understand the basics of Java programming including:

* Printing output
* Declaring variables
* String concatenation

---

## Code Explanation

### ➞ Step 1: main Method

```java
public static void main(String[] args)
```

* This is the entry point of every Java application.
* The code inside this method is executed first.

### ➞ Step 2: Print "Hello, world!"

```java
System.out.println("Hello, world!");
```

* This prints the text to the console.
* `println` prints the string and moves the cursor to a new line.

### ➞ Step 3: Declare Variables

```java
String name = "Ali";
int age = 20;
```

* `String` is used to store text.
* `int` is used to store integer numbers.
* We are creating a variable `name` with value `Ali` and an `age` variable with value `20`.

### ➞ Step 4: Print Variables with Text

```java
System.out.println("My name is " + name + " and I am " + age + " years old.");
```

* This line joins the text with variable values using `+` operator.
* It prints: `My name is Ali and I am 20 years old.`

---

## Output

```
Hello, world!
My name is Ali and I am 20 years old.
```

---

## Notes

* All Java code statements end with a semicolon `;`
* Java is **case-sensitive**: `System`, `system`, `Main`, `main` are all different.
* Always place your code inside the `main` method (for now).
