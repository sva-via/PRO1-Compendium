# Appendix A – Java Syntax Quick Reference

## Introduction

This appendix provides a compact overview of the Java syntax used throughout PRO1.

The goal is not to replace explanations from the chapters, but to provide a quick reference while working with:

- exercises
- assignments
- tests
- examples

The appendix focuses only on syntax introduced in the course.

---

# 1. Class Structure

```java
public class Person
{
  private String name;

  public Person(String name)
  {
    this.name = name;
  }

  public String getName()
  {
    return name;
  }
}
```

Main parts:

- class declaration
- fields
- constructor
- methods

---

# 2. Variables

## Primitive Variables

```java
int age = 20;
double temperature = 21.5;
boolean valid = true;
char grade = 'A';
```

---

## Reference Variables

```java
String name = "Bob";
Person person = new Person("Ada");
```

Reference variables store references to objects.

---

# 3. Primitive Types

| Type | Example |
|---|---|
| `int` | `int x = 5;` |
| `double` | `double y = 3.14;` |
| `boolean` | `boolean ok = true;` |
| `char` | `char c = 'A';` |

---

# 4. Strings

```java
String name = "Ada";
```

Useful methods:

```java
name.length()
name.toUpperCase()
name.toLowerCase()
name.trim()
name.contains("Ada")
name.substring(0, 2)
```

---

# 5. Creating Objects

```java
Person person = new Person("Bob");
```

General form:

```java
ClassName variable = new ClassName(arguments);
```

---

# 6. Fields (Instance Variables)

```java
private String name;
private int age;
```

Fields store object state.

---

# 7. Constructors

```java
public Person(String name)
{
  this.name = name;
}
```

Constructors:
- have the same name as the class
- have no return type
- initialize objects

---

# 8. Methods

## Method Returning a Value

```java
public int getAge()
{
  return age;
}
```

---

## Void Method

```java
public void birthday()
{
  age++;
}
```

---

## Boolean Method

```java
public boolean isAdult()
{
  return age >= 18;
}
```

---

# 9. this

`this` refers to the current object.

Example:

```java
this.name = name;
```

Used to distinguish fields from parameters.

---

# 10. Constructor Delegation

```java
public Person(String name)
{
  this(name, 18);
}
```

A constructor can call another constructor using `this(...)`.

---

# 11. if Statements

```java
if (age >= 18)
{
  return true;
}
```

---

## if-else

```java
if (age >= 18)
{
  return "Adult";
}
else
{
  return "Child";
}
```

---

## else-if

```java
if (age < 13)
{
  return "Child";
}
else if (age < 20)
{
  return "Teenager";
}
else
{
  return "Adult";
}
```

---

# 12. switch

```java
switch(day)
{
  case 1:
    return "Monday";

  case 2:
    return "Tuesday";

  default:
    return "Unknown";
}
```

---

# 13. Relational Operators

| Operator | Meaning |
|---|---|
| `==` | equal |
| `!=` | not equal |
| `>` | greater than |
| `<` | less than |
| `>=` | greater than or equal |
| `<=` | less than or equal |

---

# 14. Logical Operators

| Operator | Meaning |
|---|---|
| `&&` | AND |
| `||` | OR |
| `!` | NOT |

Example:

```java
if (age >= 18 && age < 65)
{
  // ...
}
```

---

# 15. Comparing Strings

Correct:

```java
name.equals("Bob")
```

Avoid:

```java
name == "Bob"
```

`equals()` compares contents.

`==` compares references.

---

# 16. null

```java
Person person = null;
```

Checking for null:

```java
if (person != null)
{
  // ...
}
```

---

# 17. Arrays

## Creating Arrays

```java
int[] numbers = new int[10];
```

---

## Accessing Elements

```java
numbers[0]
numbers[1]
```

---

## Array Length

```java
numbers.length
```

---

# 18. for Loops

```java
for (int i = 0; i < size; i++)
{
  // ...
}
```

Used frequently for arrays.

---

# 19. Enhanced for Loops

```java
for (int number : numbers)
{
  // ...
}
```

Used when indexes are unnecessary.

---

# 20. while Loops

```java
while (x > 0)
{
  x--;
}
```

---

# 21. do-while Loops

```java
do
{
  x--;
}
while (x > 0);
```

Executes at least once.

---

# 22. ArrayList

## Import

```java
import java.util.ArrayList;
```

---

## Creating an ArrayList

```java
ArrayList<String> names;
names = new ArrayList<String>();
```

---

## Adding Elements

```java
names.add("Ada");
```

---

## Accessing Elements

```java
names.get(0)
```

---

## Replacing Elements

```java
names.set(0, "Bob")
```

---

## Removing Elements

```java
names.remove(0)
```

---

## Collection Size

```java
names.size()
```

---

# 23. Exceptions

## Throwing Exceptions

```java
throw new IllegalArgumentException(
    "Illegal age");
```

---

## try-catch

```java
try
{
  // risky code
}
catch (Exception e)
{
  // handle exception
}
```

---

# 24. JUnit Basics

## Simple Test

```java
@Test void getAge()
{
  Person person = new Person("Bob", 20);

  assertEquals(20, person.getAge());
}
```

---

## Testing Exceptions

```java
@Test void illegalAge()
{
  assertThrows(IllegalArgumentException.class,
      () -> new Person("Bob", -1));
}
```

---

# 25. toString()

```java
public String toString()
{
  return name + ", age=" + age;
}
```

Provides a textual representation of the object.

---

# 26. equals()

```java
public boolean equals(Object obj)
{
  // compare object contents
}
```

Used to compare object meaning or contents.

---

# 27. LocalDate

## Import

```java
import java.time.LocalDate;
```

---

## Creating Dates

```java
LocalDate birthday = LocalDate.of(2000, 10, 25);
```

---

## Useful Methods

```java
LocalDate.now()
birthday.isAfter(LocalDate.now())
```

---

# 28. UML Visibility Symbols

| Symbol | Meaning |
|---|---|
| `+` | public |
| `-` | private |

Example:

```text
+ getName() : String
- age : int
```

---

# 29. Common Java Keywords

| Keyword | Purpose |
|---|---|
| `class` | define class |
| `public` | accessible everywhere |
| `private` | accessible only inside class |
| `new` | create object |
| `return` | return value |
| `void` | no return value |
| `this` | current object |
| `if` | selection |
| `else` | alternative branch |
| `for` | repetition |
| `while` | repetition |
| `switch` | multiple alternatives |
| `null` | no object reference |

---

# 30. Common Beginner Mistakes

Common mistakes include:

- forgetting `new`
- confusing objects and references
- using `==` for strings
- forgetting braces `{}`
- forgetting semicolons `;`
- using `length()` instead of `length`
- confusing `size()` and `length`
- accessing illegal indexes
- forgetting to initialize collections

---

# Final Remarks

This appendix is intended as a quick syntax reference during the course.

The most important goal is still:

- understanding object-oriented thinking
- assigning responsibility correctly
- designing meaningful classes
- protecting invariants
- writing readable code

Syntax is important, but design and responsibility remain the primary focus of PRO1.

