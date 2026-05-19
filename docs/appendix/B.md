# Appendix B – IntelliJ IDEA Quick Guide

## Introduction

This appendix provides a practical introduction to IntelliJ IDEA for PRO1.

The goal is not to cover every IntelliJ feature, but to explain the tools and workflows most commonly used during the course.

The guide focuses on:

- creating Java projects
- organizing exercises
- creating classes
- creating JUnit tests
- running tests
- navigating code efficiently

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

# 2. Recommended PRO1 Structure

In PRO1, it is recommended to organize work using:

- one IntelliJ project
- one module per exercise

This creates a clean and simple structure.

Example:

```text
PRO1
├── Person_v1
├── Person_v2
├── Person_v3
├── Rectangle_v1
└── Temperature_v1
```

Each exercise becomes an independent module.

Advantages:

- exercises remain separated
- testing becomes simpler
- errors are isolated
- navigation becomes easier

---

# 3. Structure of an Exercise Module

A typical module structure:

```text
Person_v1
├── src
│   └── Person.java
└── Test
    └── PersonTest.java
```

---

## src Directory

The `src` directory contains the Java classes.

Example:

```text
Person.java
Rectangle.java
Temperature.java
```

These classes contain:

- state
- behavior
- invariants
- object-oriented design

---

## Test Directory

The `Test` directory contains JUnit test classes.

Example:

```text
PersonTest.java
RectangleTest.java
```

The tests verify:

- object behavior
- calculations
- invariants
- exceptions

Separating tests from source code improves readability and structure.

---

# 4. Creating a New IntelliJ Project

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
JDK 25
```

If no JDK is installed, IntelliJ can usually download one automatically.

---

## Step 4

Choose a project name.

Example:

```text
PRO1
```

---

## Step 5

Press:

```text
Create
```

---

# 5. Creating a Module for an Exercise

Each exercise should normally be created as its own module.

---

## Step 1

Right-click the project name.

---

## Step 2

Select:

```text
New → Module
```

---

## Step 3

Choose:

```text
Java
```

---

## Step 4

Choose a module name.

Example:

```text
Person_v1
```

---

## Step 5

Press:

```text
Create
```

---

# 2. Creating the Test Directory

## Step 1

Right-click the module name.

---

## Step 2

Select:

```text
New → Directory
```

---

## Step 3

Create:

```text
Test
```

---

## Step 4

Right-click the `Test` directory.

Select:

```text
Mark Directory As → Test Sources Root
```

---

# 3. Creating a Class

## Step 1

Right-click:

```text
src
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

# 4. Creating a Test Class

## Step 1

Right-click:

```text
Test
```

---

## Step 2

Select:

```text
New → Java Class
```

---

## Step 3

Create a test class.

Example:

```text
PersonTest
```

---

## Step 4

Write JUnit tests inside the test class.

Example:

```java
@Test void getAge()
{
  Person person = new Person("Bob", 20);

  assertEquals(20, person.getAge());
}
```

---

# 5. Running Tests

JUnit tests can be run directly in IntelliJ.

---

## Run a Single Test

Click the green triangle next to the test method.

---

## Run an Entire Test Class

Click the green triangle next to the class name.

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

# 6. Useful Keyboard Shortcuts

## Search Everywhere

```text
Double Shift
```

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

---

## Reformat Code

```text
Ctrl + Alt + L
```

---

## Rename

```text
Shift + F6
```

---

## Navigate to Declaration

```text
Ctrl + Click
```

---

# 7. Common Beginner Mistakes

Common mistakes:

1. Creating classes in the wrong module
2. Forgetting to mark `Test` as Test Sources Root
3. Mixing tests and source classes
4. Forgetting imports
5. Ignoring IntelliJ warnings
6. Writing all code in one class
7. Using generated code without understanding it

---

# 8. Recommended Workflow

A recommended workflow for PRO1:

1. Create the module
2. Create the `Test` directory
3. Create the class
4. Create the test class
5. Write a small test
6. Implement the simplest code
7. Run the test
8. Improve the design
9. Repeat

This supports the:

- test-first approach
- design-first approach
- object-first approach

used throughout the course.

---

# Final Remarks

Learning IntelliJ takes practice.

Students are encouraged to:

- explore the IDE
- use keyboard shortcuts
- read error messages carefully
- run tests frequently
- organize exercises clearly
- think in terms of objects and responsibility

Efficient use of IntelliJ helps students focus more on:

- design
- testing
- responsibility
- object-oriented thinking

rather than syntax details.
