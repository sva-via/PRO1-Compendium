# Appendix D – JUnit Mini Guide

## Introduction

This appendix provides a compact introduction to JUnit testing in PRO1.

JUnit is used throughout the course to:

- test object behavior
- verify invariants
- test calculations
- test exceptions
- support object-oriented design

Testing is an important part of the course philosophy.

The course follows a strong:

- test-first
- design-first
- object-first

approach.

---

# 1. What Is JUnit?

JUnit is a Java testing framework.

JUnit allows programmers to:

- write automated tests
- verify expected behavior
- detect errors early
- document expected behavior

JUnit tests are written as normal Java methods.

---

# 2. Why Testing Matters

Testing helps verify that objects behave correctly.

Example questions:

- Does the constructor initialize correctly?
- Does a method return the correct value?
- Are invariants protected?
- Are exceptions thrown correctly?

Testing supports:

- correctness
- readability
- maintainability
- confidence during development

---

# 3. Structure of a JUnit Test

Example:

```java
@Test void getAge()
{
  Person person = new Person("Bob", 20);

  assertEquals(20, person.getAge());
}
```

A test usually contains:

1. Setup
2. Action
3. Verification

---

# 4. Importing JUnit

Typical imports:

```java
import org.junit.jupiter.api.Test;

import static org.junit.jupiter.api.Assertions.*;
```

These imports provide:
- `@Test`
- assertion methods

---

# 5. The @Test Annotation

JUnit identifies test methods using `@Test`.

Example:

```java
@Test void isAdult()
{
  // test code
}
```

Without `@Test`, the method is not executed as a test.

---

# 6. Naming Test Methods

Test names should describe behavior clearly.

Good examples:

```java
@Test void incrementOnceReturns1()
```

```java
@Test void constructorRejectsNegativeAge()
```

Poor examples:

```java
@Test void test1()
```

Readable test names help explain system behavior.

---

# 7. assertEquals

`assertEquals` checks expected values.

Example:

```java
assertEquals(20, person.getAge());
```

Structure:

```java
assertEquals(expected, actual)
```

---

# 8. Testing double Values

Floating point numbers are approximate.

Tests therefore use an epsilon value.

Example:

```java
private static final double EPSILON = 0.00001;
```

Example:

```java
assertEquals(3.14, circle.getArea(), EPSILON);
```

---

# 9. assertTrue and assertFalse

Used for boolean methods.

Example:

```java
assertTrue(person.isAdult());
```

Example:

```java
assertFalse(person.isAdult());
```

Boolean methods are common in object-oriented design.

---

# 10. assertNull and assertNotNull

Used for references.

Example:

```java
assertNull(person.getEmail());
```

Example:

```java
assertNotNull(person.getEmail());
```

---

# 11. Testing Exceptions

JUnit can verify that exceptions are thrown.

Example:

```java
@Test void negativeAgeThrowsException()
{
  assertThrows(IllegalArgumentException.class,
      () -> new Person("Bob", -1));
}
```

This is important for testing invariants and validation.

---

# 12. Understanding Lambda Expressions in Tests

Example:

```java
() -> new Person("Bob", -1)
```

This represents code that should throw the exception.

At this stage of the course, it is enough to understand:

- JUnit executes the code
- JUnit checks whether the exception occurs

Detailed lambda syntax is introduced later in the course.

---

# 13. Testing Constructors

Constructors should be tested carefully.

Example:

```java
@Test void constructorInitializesName()
{
  Person person = new Person("Bob", 20);

  assertEquals("Bob", person.getName());
}
```

Constructors are responsible for establishing valid state.

---

# 14. Testing Setters

Setter methods should preserve invariants.

Example:

```java
@Test void setAgeChangesAge()
{
  Person person = new Person("Bob", 20);

  person.setAge(25);

  assertEquals(25, person.getAge());
}
```

---

# 15. Testing Invalid State

Invalid input should also be tested.

Example:

```java
@Test void setNegativeAgeThrowsException()
{
  Person person = new Person("Bob", 20);

  assertThrows(IllegalArgumentException.class,
      () -> person.setAge(-1));
}
```

Testing invalid behavior is just as important as testing valid behavior.

---

# 16. Boundary Value Testing

Boundary values are especially important.

Example:

```text
age = 0
age = 1
age = 17
age = 18
```

Example:

```java
@Test void age18IsAdult()
{
  Person person = new Person("Bob", 18);

  assertTrue(person.isAdult());
}
```

---

# 17. Testing Arrays and Collections

Collections should also be tested.

Example:

```java
@Test void addGradeIncreasesSize()
{
  GradeList list = new GradeList();

  list.addGrade(12);

  assertEquals(1, list.size());
}
```

Important test cases include:

- empty collections
- adding elements
- removing elements
- searching
- boundary indexes

---

# 18. Testing Object Collaboration

Associations should also be tested.

Example:

```java
@Test void addStudent()
{
  SchoolClass c = new SchoolClass();
  Student s = new Student("Ada");

  c.addStudent(s);

  assertEquals(1, c.numberOfStudents());
}
```

Object relationships are important in later sessions.

---

# 19. Arrange – Act – Assert

A common structure for tests:

## Arrange

Create objects and test data.

## Act

Call the method being tested.

## Assert

Verify the result.

Example:

```java
@Test void birthdayIncreasesAge()
{
  // Arrange
  Person person = new Person("Bob", 20);

  // Act
  person.birthday();

  // Assert
  assertEquals(21, person.getAge());
}
```

This structure improves readability.

---

# 20. Good Testing Principles

Good tests should:

- be small
- focus on one behavior
- have readable names
- be independent
- test observable behavior

Tests should not depend on:

- console output
- execution order
- hidden internal details

---

# 21. What Should Be Tested?

Important areas:

## Constructors

- correct initialization
- invalid input

## Methods

- calculations
- state changes
- boolean behavior

## Invariants

- valid state
- invalid state

## Collections

- insertion
- removal
- searching

## Associations

- adding objects
- removing objects
- collaboration

---

# 22. Common Beginner Mistakes

Common mistakes:

1. Forgetting `@Test`
2. Testing multiple behaviors in one test
3. Using unclear test names
4. Forgetting boundary cases
5. Only testing valid input
6. Using console output instead of assertions
7. Forgetting epsilon for `double`
8. Writing tests dependent on other tests

---

# 23. JUnit and Course Philosophy

Testing is not an optional extra.

In PRO1, testing is part of:

- understanding object behavior
- understanding responsibility
- protecting invariants
- designing maintainable systems

JUnit supports object-oriented thinking.

---

# 24. Recommended Workflow

A recommended workflow:

1. Design the class
2. Write a small test
3. Implement minimal code
4. Run the test
5. Improve the design
6. Add more tests

This supports:

- test-first thinking
- incremental development
- better design decisions

---

# Final Remarks

JUnit is an essential tool in modern software development.

The goal is not simply to make tests pass.

The real goal is to:
- understand behavior
- protect invariants
- support design
- create reliable software

Good tests help programmers think clearly about object responsibility and expected behavior.

