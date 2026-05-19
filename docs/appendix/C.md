# Appendix C – Scanner and Console I/O

## Introduction

This appendix introduces basic console input and output in Java.

The appendix explains:

- console output
- console input using `Scanner`
- reading primitive values and strings
- common input problems

---

## Important Note About PRO1

The PRO1 course is primarily:

- object-oriented
- design-focused
- test-focused

The course does **not** focus heavily on console programs.

Most course examples therefore avoid:

- `main`
- console menus
- large console applications
- extensive use of `System.out.println`

However, understanding simple console I/O is still useful for:

- small experiments
- debugging
- simple demonstrations
- understanding basic program interaction

---

## 1. Console Output

Java can print text to the console.

Example:

```java
System.out.println("Hello world");
```

`println` means:

```text
print line
```

A newline is added automatically.

---

### Printing Variables

Example:

```java
int age = 20;

System.out.println(age);
```

Example:

```java
String name = "Ada";

System.out.println(name);
```

---

### Concatenating Output

Strings can be combined using `+`.

Example:

```java
String name = "Bob";
int age = 20;

System.out.println(name + " is " + age + " years old");
```

---

## 2. The main Method

Console programs usually begin with a `main` method.

Example:

```java
public class Main
{
  public static void main(String[] args)
  {
    System.out.println("Hello world");
  }
}
```

The `main` method is the program entry point.

---

### Important Course Note

The PRO1 course generally avoids using `main` in exercises.

The course focuses instead on:

- objects
- classes
- methods
- testing

You should therefore think of console examples as supplementary material.

---

## 3. Scanner

`Scanner` reads input from the console.

The class must first be imported.

Example:

```java
import java.util.Scanner;
```

---

## 4. Creating a Scanner

Example:

```java
Scanner input = new Scanner(System.in);
```

Explanation:

| Part | Meaning |
|---|---|
| `Scanner` | class type |
| `input` | variable name |
| `new Scanner(...)` | creates scanner object |
| `System.in` | console input stream |

---

## 5. Reading Strings

Example:

```java
Scanner input = new Scanner(System.in);

System.out.print("Name: ");
String name = input.nextLine();
```

`nextLine()` reads an entire line of text.

---

## 6. Reading int Values

Example:

```java
Scanner input = new Scanner(System.in);

System.out.print("Age: ");
int age = input.nextInt();
```

`nextInt()` reads an integer.

---

## 7. Reading double Values

Example:

```java
Scanner input = new Scanner(System.in);

System.out.print("Temperature: ");
double temp = input.nextDouble();
```

`nextDouble()` reads decimal values.

---

## 8. Reading boolean Values

Example:

```java
Scanner input = new Scanner(System.in);

System.out.print("Adult? ");
boolean adult = input.nextBoolean();
```

Accepted values are usually:

```text
true
false
```

---

## 9. Common Scanner Problem

A common beginner problem occurs when mixing:

- `nextInt()`
- `nextDouble()`
- `nextLine()`

Example:

```java
int age = input.nextInt();
String name = input.nextLine();
```

The newline after the integer remains in the input buffer.

As a result:

```java
name
```

may become an empty string.

---

## 10. Fixing the nextLine Problem

A common solution:

```java
int age = input.nextInt();
input.nextLine();

String name = input.nextLine();
```

The extra `nextLine()` consumes the remaining newline.

---

## 11. Example Console Program

Example:

```java
import java.util.Scanner;

public class Main
{
  public static void main(String[] args)
  {
    Scanner input = new Scanner(System.in);

    System.out.print("Name: ");
    String name = input.nextLine();

    System.out.print("Age: ");
    int age = input.nextInt();

    System.out.println(name + " is " + age + " years old");
  }
}
```

---

## 12. Scanner and Exceptions

Invalid input may cause exceptions.

Example:

```text
InputMismatchException
```

Example:

```java
int age = input.nextInt();
```

If the user enters:

```text
hello
```

an exception occurs.

---

## 13. Simple try-catch Example

Example:

```java
try
{
  int age = input.nextInt();
}
catch (InputMismatchException e)
{
  System.out.println("Illegal number");
}
```

This topic becomes more important later in the course.

---

## 14. Closing the Scanner

A scanner can be closed.

Example:

```java
input.close();
```

For simple beginner programs this is often not emphasized heavily.

---

## 15. Console Programs vs Object-Oriented Design

Console I/O should usually be separated from domain logic.

Less good:

```java
public class Person
{
  public void readAgeFromConsole()
  {
    // scanner logic
  }
}
```

Better:

- keep console code separate
- keep domain classes focused on responsibility

Domain classes should mainly represent:

- state
- behavior
- invariants

not user interface logic.

---

## 16. Console I/O and Testing

Console programs are difficult to test automatically.

This is one reason why the course emphasizes:

- object methods
- return values
- JUnit testing

instead of interactive console programs.

Example:

Good:

```java
person.isAdult()
```

Less good:

```java
System.out.println("Adult")
```

The first approach is easier to test.

---

## 17. Recommended Use in PRO1

Use console I/O mainly for:

- experiments
- debugging
- small demonstrations

The primary focus of the course remains:

- object-oriented thinking
- class design
- testing
- encapsulation
- responsibility

---

## 18. Common Beginner Mistakes

Common mistakes:

1. Forgetting to import `Scanner`
2. Forgetting `new Scanner(System.in)`
3. Mixing `nextInt()` and `nextLine()` incorrectly
4. Forgetting semicolons
5. Writing all logic inside `main`
6. Placing domain logic inside console code
7. Using console output instead of return values

---

## 19. Reflection Questions

- What is the purpose of `Scanner`?
- Why does `nextLine()` sometimes return an empty string?
- Why are conso
