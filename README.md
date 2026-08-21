# CS1 Review and Readiness Guide

### Purpose

This guide reviews the most important concepts from Computer Science I that students are expected to know before beginning Computer Science II.

The goal is **not to memorize syntax**. Students should be able to read, trace, explain, modify, and write programs.

---

# Part I — Variables, Types, and Expressions

## Key Concepts

Students should be comfortable with:

* Primitive data types
* Variables and assignment
* Integer and floating-point arithmetic
* Type conversion
* Boolean expressions
* Operator precedence
* Integer division
* Modulus

### Example Questions

**1. What is printed?**

```java
int x = 17;
int y = 5;

System.out.println(x / y);
System.out.println(x % y);
System.out.println((double) x / y);
```

**2. What is the value of `result`?**

```java
int a = 7;
int b = 3;
double result = a / b;
```

Explain why.

**3. Write a Java expression that determines whether an integer `n` is even.**

**4. Write a Java expression that determines whether `n` is between 10 and 20 inclusive.**

**5. What is wrong with this code?**

```java
int x = 10;
double y = x / 4;
```

How could you modify it if you want `y` to be `2.5`?

---

# Part II — Conditional Statements

## Key Concepts

* `if`
* `if-else`
* Nested conditionals
* `else-if`
* Boolean expressions
* Logical operators

### Example Questions

**6. What does the following program print?**

```java
int x = 15;

if (x > 20)
    System.out.println("A");
else if (x > 10)
    System.out.println("B");
else
    System.out.println("C");
```

**7. Rewrite the following using a single Boolean expression.**

```java
if (age >= 18) {
    if (hasLicense) {
        System.out.println("Can drive");
    }
}
```

**8. Identify the logical error.**

```java
if (x >= 0 || x <= 100)
    System.out.println("Valid");
```

What was the programmer probably trying to write?

**9. Write a program segment that prints:**

```text
A  if score >= 90
B  if score >= 80
C  if score >= 70
D  if score >= 60
F  otherwise
```

---

# Part III — Loops

## Key Concepts

Students should understand:

* `for`
* `while`
* `do-while`
* Loop initialization
* Loop condition
* Loop update
* Nested loops
* Infinite loops
* Off-by-one errors

---

## Trace the Loop

**10. What is printed?**

```java
for (int i = 1; i <= 5; i++) {
    System.out.print(i + " ");
}
```

**11. What is printed?**

```java
int i = 10;

while (i > 0) {
    System.out.print(i + " ");
    i -= 3;
}
```

**12. How many times does the loop execute?**

```java
for (int i = 0; i < 100; i += 5) {
    System.out.println(i);
}
```

---

## Write a Loop

**13. Write a loop that prints:**

```text
1 2 3 4 5 6 7 8 9 10
```

**14. Write a loop that prints all even numbers from 2 through 100.**

**15. Write a loop that calculates the sum:**

$$
1 + 2 + 3 + \cdots + 100
$$

**16. Write a program segment that counts how many digits are in a positive integer.**

For example:

```text
Input: 58291
Output: 5
```

---

# Part IV — Nested Loops

### Example Questions

**17. What does this program print?**

```java
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 4; j++) {
        System.out.print("*");
    }
    System.out.println();
}
```

**18. Modify the program to print:**

```text
*
**
***
****
*****
```

**19. What is the Big-O complexity of the following code?**

```java
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        System.out.println(i + " " + j);
    }
}
```

---

# Part V — Methods

## Key Concepts

Students should understand:

* Method declaration
* Parameters
* Return values
* `void`
* Local variables
* Scope
* Method calls
* Pass-by-value

### Example Questions

**20. Write a method:**

```java
public static int square(int n)
```

that returns the square of `n`.

---

**21. Write a method:**

```java
public static boolean isEven(int n)
```

that returns `true` if `n` is even.

---

**22. What does this method return?**

```java
public static int mystery(int x, int y) {
    return x * 2 + y;
}
```

What is:

```java
mystery(4, 7)
```

?

---

**23. Find the error.**

```java
public static int maximum(int a, int b) {
    if (a > b)
        return a;
}
```

Why won't this compile?

---

# Part VI — Scope

**24. What is printed?**

```java
int x = 10;

if (x > 5) {
    int y = 20;
    System.out.println(x + y);
}

System.out.println(x);
```

Can you access `y` after the `if` statement?

---

**25. Explain the difference between a local variable and a parameter.**

---

# Part VII — Arrays

This is one of the most important CS1 topics for CS2.

## Key Concepts

* Declaring arrays
* Creating arrays
* Indexing
* `length`
* Traversing arrays
* Searching
* Finding minimum/maximum
* Array mutation
* Off-by-one errors

### Example Questions

**26. What is printed?**

```java
int[] a = {4, 7, 2, 9, 5};

System.out.println(a[0]);
System.out.println(a[3]);
System.out.println(a.length);
```

---

**27. What is wrong with this loop?**

```java
for (int i = 0; i <= a.length; i++) {
    System.out.println(a[i]);
}
```

---

## Array Programming

**28. Write a method that returns the sum of an array.**

```java
public static int sum(int[] a)
```

---

**29. Write a method that returns the largest value in an array.**

```java
public static int max(int[] a)
```

---

**30. Write a method that returns the number of even values in an array.**

```java
public static int countEven(int[] a)
```

---

**31. Write a method that searches an array for a target value.**

```java
public static int linearSearch(int[] a, int target)
```

Return the index if found and `-1` otherwise.

---

**32. What is the Big-O complexity of linear search?**

---

# Part VIII — Array Tracing

Consider:

```java
int[] a = {3, 1, 4, 1, 5};

for (int i = 0; i < a.length; i++) {
    a[i] *= 2;
}
```

**33. What is the final contents of `a`?**

---

Now consider:

```java
int[] a = {3, 1, 4, 1, 5};

for (int i = 0; i < a.length - 1; i++) {
    if (a[i] > a[i + 1]) {
        int temp = a[i];
        a[i] = a[i + 1];
        a[i + 1] = temp;
    }
}
```

**34. What is the final contents of the array?**

**35. What algorithmic idea does this resemble?**

---

# Part IX — Strings

## Key Concepts

* String indexing
* `length()`
* `charAt()`
* `substring()`
* String comparison
* Traversing characters
* Immutability

### Example Questions

**36. What is printed?**

```java
String s = "Computer";

System.out.println(s.length());
System.out.println(s.charAt(0));
System.out.println(s.charAt(3));
```

---

**37. What is wrong with this?**

```java
if (name == "Alice") {
    System.out.println("Hello");
}
```

How should strings normally be compared in Java?

---

**38. Write a method that counts the number of vowels in a string.**

```java
public static int countVowels(String s)
```

---

**39. Write a method that determines whether a string is a palindrome.**

Examples:

```text
radar → true
hello → false
```

---

# Part X — ArrayList

If `ArrayList` was introduced in CS1, students should review:

* Creating an `ArrayList`
* `add`
* `get`
* `set`
* `remove`
* `size`
* Traversal

### Example Questions

**40. What is printed?**

```java
ArrayList<Integer> list = new ArrayList<>();

list.add(10);
list.add(20);
list.add(30);

list.set(1, 50);

System.out.println(list);
```

---

**41. What is the difference between:**

```java
list.remove(2);
```

and

```java
list.remove(Integer.valueOf(2));
```

---

# Part XI — Classes and Objects

CS2 students should be comfortable with basic object-oriented programming.

## Key Concepts

* Classes
* Objects
* Fields
* Constructors
* Methods
* Access modifiers
* Encapsulation
* `this`

### Example

Given:

```java
public class Student {
    private String name;
    private double gpa;

    public Student(String name, double gpa) {
        this.name = name;
        this.gpa = gpa;
    }

    public double getGpa() {
        return gpa;
    }
}
```

### Questions

**42. Create a `Student` object named `s`.**

**43. How do you call `getGpa()`?**

**44. Why are the fields declared `private`?**

**45. What is the purpose of `this.name = name`?**

---

# Part XII — References

This is an especially important CS2 readiness topic.

Consider:

```java
int[] a = {1, 2, 3};
int[] b = a;

b[0] = 100;
```

**46. What is the value of `a[0]`?**

**47. Why?**

---

Now consider:

```java
Student s1 = new Student("Alice", 3.8);
Student s2 = s1;
```

**48. How many Student objects have been created?**

**49. What does `s1 == s2` mean?**

---

# Part XIII — Recursion

Students entering CS2 should understand the basic structure of recursive methods.

### Example

```java
public static int factorial(int n) {
    if (n == 0)
        return 1;

    return n * factorial(n - 1);
}
```

**50. What is the base case?**

**51. What is the recursive case?**

**52. What does `factorial(4)` return?**

---

### Write Recursion

**53. Write a recursive method that calculates:**

[
1 + 2 + \cdots + n
]

---

**54. Write a recursive method that prints the integers from `n` down to `1`.**

---

# Part XIV — Searching and Sorting

Students should have at least a basic understanding of:

* Linear search
* Binary search
* Selection sort
* Insertion sort
* Bubble sort
* `Arrays.sort()`

### Questions

**55. What is the major requirement for binary search?**

**56. What is the Big-O complexity of binary search?**

**57. What is the Big-O complexity of linear search?**

**58. Why can't binary search normally be applied directly to an unsorted array?**

---

# Part XV — Algorithm Analysis

Students should be able to classify simple algorithms.

### Question 59

Determine the Big-O complexity:

```java
for (int i = 0; i < n; i++) {
    System.out.println(i);
}
```

---

### Question 60

Determine the Big-O complexity:

```java
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        System.out.println(i + j);
    }
}
```

---

### Question 61

Determine the Big-O complexity:

```java
int i = n;

while (i > 1) {
    i /= 2;
}
```

---

### Question 62

Which grows faster as `n` becomes large?

```text
n
n * log n
n²
2ⁿ
n!
```

Put them in increasing order.

---

# Part XVI — Debugging

Give students code containing common mistakes.

### Question 63

Find the error:

```java
int sum = 0;

for (int i = 0; i < a.length; i++) {
    sum = i;
}
```

What should the code probably do?

---

### Question 64

Find the error:

```java
int count = 0;

for (int i = 0; i <= a.length; i++) {
    if (a[i] > 0)
        count++;
}
```

---

### Question 65

Find the error:

```java
int max = 0;

for (int x : a) {
    if (x > max)
        max = x;
}
```

Give an example of an array for which this produces the wrong answer.

---

# Part XVII — Problem-Solving Questions

These are more important than syntax questions.

### Question 66 — Digit Sum

Write a method that takes a positive integer and returns the sum of its digits.

Example:

```text
Input: 5832
Output: 18
```

---

### Question 67 — Reverse an Array

Write a method that reverses an array **in place**.

Example:

```text
Before:  1 2 3 4 5
After:   5 4 3 2 1
```

---

### Question 68 — Second Largest

Write a method that returns the second-largest value in an integer array.

Discuss what should happen if the array contains duplicate values.

---

### Question 69 — Remove Duplicates

Given a sorted array, determine how many distinct values it contains.

Example:

```text
1 1 2 2 2 4 5 5

Answer: 4
```

---

### Question 70 — Frequency Counting

Given an array of integers, determine which value occurs most frequently.

---

# Part XVIII — CS1 Readiness Challenge

Give students this problem at the end of the review.

## Problem: Most Frequent Character

Write a method:

```java
public static char mostFrequent(String s)
```

that returns the character occurring most frequently in `s`.

Example:

```text
Input:
"banana"

Output:
'a'
```

Students should explain:

1. Their algorithm
2. Their data structure
3. Their time complexity
4. What happens if there is a tie

---

# Suggested In-Class Diagnostic

Rather than giving students all 70 questions, I would administer a **60–75 minute diagnostic** during the first class.

## Section A — Trace Code

5 questions × 2 points = 10 points

Topics:

* Expressions
* Conditionals
* Loops
* Arrays
* Methods

## Section B — Find the Bug

5 questions × 2 points = 10 points

Topics:

* Off-by-one
* Incorrect condition
* Wrong accumulator
* String comparison
* Array indexing

## Section C — Write Code

4 questions × 5 points = 20 points

1. Sum an array
2. Find maximum
3. Linear search
4. String processing

## Section D — Recursion and Complexity

5 questions × 2 points = 10 points

## Section E — Challenge Problem

1 problem × 10 points

**Total: 60 points**

---

# Suggested Review Schedule

## Class 1 — Programming Fundamentals

Review:

* Variables
* Expressions
* Conditionals
* Loops
* Methods

Practice:

* Code tracing
* Short programming exercises

---

## Class 2 — Arrays and Strings

Review:

* Arrays
* Array traversal
* Searching
* Strings
* ArrayList

Practice:

* Array problems
* String problems

---

## Class 3 — Object-Oriented Programming

Review:

* Classes
* Objects
* Constructors
* Encapsulation
* References

Practice:

* Small class implementation

---

## Class 4 — Recursion and Algorithms

Review:

* Recursion
* Searching
* Sorting
* Big-O

Practice:

* Recursion exercises
* Complexity exercises

---

## Class 5 — CS1 Review Challenge

Give students a **90-minute programming contest** containing approximately 5–7 problems.

Example progression:

```text
Problem A — Basic loops
Problem B — Arrays
Problem C — Strings
Problem D — Methods
Problem E — ArrayList
Problem F — Recursion
Problem G — Challenge problem
```

This gives you much better information about students' actual CS1 readiness than a conventional written exam.

---

# CS2 Readiness Checklist

Before moving into CS2 material, students should be able to check:

* [ ] I can trace a Java program without running it.
* [ ] I can write `if/else` statements correctly.
* [ ] I can write `for` and `while` loops.
* [ ] I understand loop boundaries and off-by-one errors.
* [ ] I can write methods with parameters and return values.
* [ ] I understand variable scope.
* [ ] I can traverse an array.
* [ ] I can search an array.
* [ ] I can find the minimum/maximum of an array.
* [ ] I can manipulate strings.
* [ ] I understand basic `ArrayList` operations.
* [ ] I understand classes and objects.
* [ ] I understand references and object aliases.
* [ ] I can write a simple recursive method.
* [ ] I understand linear and binary search.
* [ ] I understand basic sorting algorithms.
* [ ] I can determine the Big-O complexity of simple code.
* [ ] I can debug a small Java program.
* [ ] I can solve a small programming problem without step-by-step instructions.

---

# Instructor Recommendation

For CS2, I would **not spend two weeks lecturing through this material**.

A better approach is:

**Day 1:** Diagnostic assessment
**Day 2:** Review weaknesses revealed by diagnostic
**Days 3–5:** Targeted programming practice
**Day 6:** CS1 programming challenge
**Day 7:** Begin CS2

The diagnostic should determine what you review.

For example, if 80% of the class can write loops but 40% cannot correctly manipulate arrays, don't spend a lecture reviewing `for` loops. Spend the time on arrays, references, and problem solving.

Most importantly, make the review **code-centered rather than definition-centered**. A student who can define a loop but cannot correctly write a loop to find the second-largest element is not yet ready for CS2.
