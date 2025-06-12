# Topic 3 – Conditional Statements in Java

## 🔹 Objective

Understand and practice using conditional statements in Java including:

* if
* if-else
* else-if ladder
* switch

---

## 🧪 Code Explanation

### ➞ Step 1: Import Scanner and Start Main Method

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
```

* `Scanner` is used to take input from the user.
* The `main` method is the entry point of the Java program.

### ➞ Step 2: if Statement

```java
System.out.print("Enter a number: ");
int number = input.nextInt();
if (number > 0) {
    System.out.println("The number is positive.");
}
```

* This checks if the number is greater than 0.
* If true, it prints that the number is positive.

### ➞ Step 3: if-else Statement

```java
System.out.print("Enter another number: ");
int number2 = input.nextInt();
if (number2 % 2 == 0) {
    System.out.println("Even number.");
} else {
    System.out.println("Odd number.");
}
```

* Checks if the number is divisible by 2.
* If yes, it's even; otherwise, odd.

### ➞ Step 4: else-if Ladder

```java
System.out.print("Enter your marks: ");
int marks = input.nextInt();
if (marks >= 90) {
    System.out.println("Grade: A+");
} else if (marks >= 80) {
    System.out.println("Grade: A");
} else if (marks >= 70) {
    System.out.println("Grade: B");
} else if (marks >= 60) {
    System.out.println("Grade: C");
} else {
    System.out.println("Fail");
}
```

* Used to check multiple ranges.
* Outputs the appropriate grade based on input marks.

### ➞ Step 5: switch Statement

```java
System.out.print("Enter day number (1 to 7): ");
int day = input.nextInt();
switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    case 4:
        System.out.println("Thursday");
        break;
    case 5:
        System.out.println("Friday");
        break;
    case 6:
        System.out.println("Saturday");
        break;
    case 7:
        System.out.println("Sunday");
        break;
    default:
        System.out.println("Invalid day number.");
}

input.close();
```

* Switch is used for exact value matching.
* Based on the day number input, prints the day name.
* `default` handles invalid inputs.

---

## ✅ Output

```
Enter a number: 5
The number is positive.

Enter another number: 8
Even number.

Enter your marks: 82
Grade: A

Enter day number (1 to 7): 5
Friday
```

---

## 📘 Notes

* Conditional statements help control program flow.
* `if`, `if-else`, and `switch` help you make decisions based on conditions.
* Always close your `Scanner` object to avoid warnings: `input.close();`
* `switch` is useful for checking against exact values, especially when there are many fixed options.
