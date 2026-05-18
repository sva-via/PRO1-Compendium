# Appendix B – IntelliJ IDEA Quick Guide

## Introduction

This appendix provides a practical introduction to IntelliJ IDEA for PRO1.

The goal is not to cover every IntelliJ feature, but to explain the tools and workflows most commonly used during the course.

The guide focuses on:

- creating Java projects
- creating classes
- running JUnit tests
- navigating code
- working efficiently in IntelliJ

---

# 1. What Is IntelliJ IDEA?

IntelliJ IDEA is an Integrated Development Environment (IDE).

An IDE helps programmers:

- write code
- organize projects
- run programs
- run tests
- detect errors
- navigate code

The course primarily uses IntelliJ IDEA Community Edition.

---

# 2. Creating a New Project

## Step 1

Open IntelliJ IDEA.

Select:

```text
New Project
```

---

## Step 2

Choose:

```text
Java
```

---

## Step 3

Choose the correct JDK.

Example:

```text
JDK 21
```

If no JDK is installed, IntelliJ can usually download one automatically.

---

## Step 4

Choose a project name.

Example:

```text
PRO1-Exercises
```

---

## Step 5

Press:

```text
Create
```

---

# 3. Understanding the Project Structure

A typical project structure:

```text
src
├── main
│   └── java
└── test
    └── java
```

---

## main/java

Contains the application classes.

Example:

```text
Person.java
Rectangle.java
Temperature.java
```

---

## test/java

Contains JUnit test classes.

Example:

```text
PersonTest.java
RectangleTest.java
```

Keeping production code and test code separated is important.

---

# 4. Creating a Class

## Step 1

Right-click:

```text
src/main/java
```

---

## Step 2

Select:

```text
New → Java Class
```

---

## Step 3

Enter the class name.

Example:

```text
Person
```

---

## Step 4

Press:

```text
Enter
```

IntelliJ creates the class automatically.

---

# 5. Creating a Test Class

## Step 1

Right-click the class name.

Example:

```text
Person
```

---

## Step 2

Select:

```text
Generate → Test
```

---

## Step 3

Choose:

```text
JUnit 5
```

---

## Step 4

Select methods to test.

---

## Step 5

Press:

```text
OK
```

The test class is usually created in:

```text
src/test/java
```

---

# 6. Running Tests

JUnit tests can be run directly in IntelliJ.

## Run a Single Test

Click the green triangle next to the test method.

Example:

```java
@Test void getAge()
{
  // ...
}
```

---

## Run an Entire Test Class

Click the green triangle next to the class name.

Example:

```java
public class PersonTest
```

---

## Test Results

### Green

```text
Tests passed
```

### Red

```text
Tests failed
```

IntelliJ shows:

- which tests failed
- expected values
- actual values
- stack traces

---

# 7. Useful Keyboard Shortcuts

## Search Everywhere

```text
Double Shift
```

Searches:

- classes
- files
- methods
- actions

---

## Generate Code

```text
Alt + Insert
```

Useful for generating:

- constructors
- getters
- setters
- `toString()`
- `equals()`

---

## Quick Fix

```text
Alt + Enter
```

Shows IntelliJ suggestions.

Examples:

- import missing classes
- create methods
- fix syntax problems

---

## Reformat Code

```text
Ctrl + Alt + L
```

Automatically formats the code.

---

## Rename

```text
Shift + F6
```

Renames variables, methods, or classes safely.

---

## Navigate to Declaration

```text
Ctrl + Click
```

Navigates directly to:

- method definitions
- class definitions
- variable declarations

---

# 8. Common IntelliJ Icons

| Icon | Meaning |
|---|---|
| Green triangle | run |
| Red underline | syntax error |
| Yellow underline | warning |
| Blue class icon | class |
| Green circle in tests | test passed |
| Red circle in tests | test failed |

---

# 9. Reading Error Messages

Error messages are important.

Common examples:

## Cannot Resolve Symbol

Example:

```text
Cannot resolve symbol 'ArrayList'
```

Often caused by:

- missing import
- spelling mistakes

---

## ';' Expected

Usually caused by:
- missing semicolon

Example:

```java
int x = 5
```

Correct:

```java
int x = 5;
```

---

## Incompatible Types

Example:

```text
Required: String
Found: int
```

The assigned value has the wrong type.

---

# 10. Working with JUnit

JUnit tests should normally be written continuously during development.

Example:

```java
@Test void isAdult()
{
  Person person = new Person("Bob", 20);

  assertTrue(person.isAdult());
}
```

The course strongly emphasizes:

- testing behavior
- testing invariants
- testing boundary values

---

# 11. IntelliJ and Imports

IntelliJ usually adds imports automatically.

Example:

```java
import java.util.ArrayList;
import java.time.LocalDate;
```

If imports are missing:

```text
Alt + Enter
```

usually fixes the problem.

---

# 12. Packages

Packages organize classes.

Example:

```java
package model;
```

Packages help structure larger systems.

Early exercises may use very simple package structures.

---

# 13. Code Completion

IntelliJ provides code completion.

Example:

```java
person.
```

IntelliJ suggests:

- methods
- fields
- variables

Code completion helps:

- reduce typing
- discover available methods
- avoid spelling mistakes

---

# 14. Refactoring

Refactoring means improving code structure without changing behavior.

IntelliJ supports safe refactoring.

Examples:
- rename methods
- rename variables
- extract methods
- move classes

Refactoring is important for maintaining readable code.

---

# 15. Common Beginner Mistakes in IntelliJ

Common mistakes:
1. Writing classes inside the wrong folder
2. Forgetting to create tests
3. Ignoring warnings and errors
4. Running the wrong test class
5. Forgetting imports
6. Misunderstanding package structure
7. Using generated code without understanding it

---

# 16. Recommended Workflow

A recommended workflow for PRO1:

1. Create the class
2. Create the test class
3. Write a small test
4. Implement the simplest code
5. Run the test
6. Improve the design
7. Repeat

This supports the test-first and design-first approach of the course.

---

# 17. IntelliJ and Course Philosophy

IntelliJ is a tool.

The most important goal is still:

- understanding object-oriented thinking
- assigning responsibility correctly
- designing meaningful classes
- protecting invariants
- writing readable code

The IDE supports these activities but does not replace understanding.

---

# Final Remarks

Learning IntelliJ takes pract
