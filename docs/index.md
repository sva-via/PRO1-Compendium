# PRO1 Compendium


## Quick start

- **Start here:** [Chapter 1 – What is an object?](chapter/01.md)
- **Appendix:** [Appendix A – Java-syntaks quick reference](appendix/A.md)


## Introduction

Welcome to the PRO1 compendium.

This compendium supports the course:

**Programming 1 – Software Engineering**

The purpose of the course is not only to learn Java syntax, but to learn how to:

- think object-oriented
- model problem domains
- design classes and objects
- assign responsibility correctly
- write readable and maintainable software
- test object behavior systematically

The course uses Java as the programming language, but the primary focus is object-oriented design.

---

## Course Philosophy

The course follows an:

- object-first
- design-first
- test-first

approach.

This means that the course focuses first on:

- objects
- responsibility
- encapsulation
- collaboration
- domain modelling

rather than:

- console menus
- procedural programming
- large algorithms
- advanced syntax

The goal is to understand how software systems are built from collaborating objects.

---

## Learning Goals

The course aims to give students the ability to:

- analyse simple problem domains
- design classes and objects
- implement Java classes from UML diagrams
- model domains using UML
- work with encapsulation and invariants
- create associations between objects
- work with arrays and collections
- test object behavior using JUnit
- handle exceptions correctly
- design maintainable object-oriented systems

Later sessions also introduce:

- inheritance
- polymorphism
- GUI programming
- file handling
- persistence
- event-driven programming

---

## Focus of the Course

The course focuses strongly on responsibility and design.

Students should continuously ask:

- Which object should be responsible?
- Which class should contain the logic?
- Which data belongs to which object?
- How should objects collaborate?
- How can invariants be protected?

Good object-oriented design is largely about assigning responsibilities correctly.

---

# How to Use This Compendium

Each chapter corresponds to a course session.

Each chapter focuses on:

- the main concepts introduced in the session
- the design ideas behind the examples
- common beginner mistakes
- important object-oriented principles

The compendium is intended to:

- support the lectures
- support exercises and assignments
- help students review concepts
- help students prepare for tests and exams

---

## Recommended Way to Study

The course is cumulative.

New concepts build on earlier sessions.

A recommended study process:

1. Read the chapter before class
2. Attend the lecture and discussions
3. Study the examples carefully
4. Implement small examples yourself
5. Write and run JUnit tests
6. Reflect on object responsibility and design
7. Review the chapter after the session

Understanding the ideas behind the code is more important than memorizing syntax.

---

## Important Design Principles

Throughout the course, several core principles are repeated.

### Encapsulation

Objects should protect their own state.

Internal data should usually remain private.

---

### Responsibility

Logic should belong inside the responsible object.

Good design:

```java
person.isAdult()
```

Less good:

```java
person.getAge() >= 18
```

---

### Invariants

Objects should always remain valid.

Constructors establish valid state.

Methods preserve valid state.

---

### Collaboration

Objects solve problems by collaborating with other objects.

Associations and collections become increasingly important later in the course.

---

### Readability

Readable code is important.

Code should:

- communicate intent clearly
- use meaningful method names
- avoid duplication
- express responsibility clearly

---

## Testing

Testing is introduced early in the course.

JUnit tests are used to:

- verify behavior
- validate object state
- test boundary cases
- test exceptions

The course emphasizes:

- testing object behavior
- testing invariants
- testing both valid and invalid cases

Testing is considered part of normal software development.

---

## UML and Design

UML diagrams are used throughout the course.

Students should learn to:

- read UML class diagrams
- understand relationships between classes
- translate UML into Java code
- model simple domains using UML

The focus is not advanced UML notation, but understanding how design maps to implementation.

---

## Course Progression

The course gradually introduces more advanced object-oriented concepts.

### Early Sessions

Focus on:

- classes
- objects
- methods
- constructors
- state and behavior
- testing

### Middle Sessions

Focus on:

- invariants
- encapsulation
- responsibility
- arrays
- loops
- collections
- object collaboration

### Later Sessions

Focus on:

- inheritance
- polymorphism
- exceptions
- file handling
- GUI applications
- persistence
- event-driven systems

Each topic builds on earlier understanding.

---

## Common Beginner Challenges

Many students initially struggle with:

- understanding references
- separating objects from variables
- assigning responsibility correctly
- understanding encapsulation
- designing meaningful classes
- understanding collections and object relationships

This is normal.

Object-oriented thinking develops gradually through practice.

---

## About the Examples

The examples in this compendium are intentionally small.

The goal is to:

- focus on concepts clearly
- avoid unnecessary complexity
- emphasize design ideas
- support learning step-by-step

Examples are chosen to illustrate:

- object responsibility
- invariants
- collaboration
- readability
- testing

---

## Preparing for the Exam

The oral exam focuses on:

- understanding UML diagrams
- designing classes
- implementing object-oriented solutions
- explaining design decisions
- writing correct Java code

Success in the course requires:

- active practice
- writing code regularly
- understanding concepts deeply
- thinking in terms of objects and responsibilities

---

## Final Remarks

Object-oriented programming is not only about writing code.

It is about:

- modelling domains
- designing collaborating objects
- protecting object validity
- assigning responsibility clearly
- creating understandable software systems

The goal of this course is to help students develop both:

- practical programming skills
- object-oriented design thinking

The compendium should be used as a guide throughout the course and as support when working with exercises, assignments, and exam preparation.

