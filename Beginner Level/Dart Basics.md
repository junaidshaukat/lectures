# Dart Basics

Welcome to the Dart Basics section! This guide covers fundamental Dart concepts including syntax and structure, variables and data types, basic operators, control flow, functions and methods, and error handling. Each section includes examples to illustrate the concepts.

## Table of Contents

1. [Syntax and Structure](#syntax-and-structure)
2. [Variables and Data Types](#variables-and-data-types)
3. [Basic Operators](#basic-operators)
4. [Control Flow](#control-flow)
   - [if Statement](#if-statement)
   - [switch Statement](#switch-statement)
   - [Loops](#loops)
5. [Functions and Methods](#functions-and-methods)
6. [Error Handling](#error-handling)

## Syntax and Structure

Dart syntax is clean and straightforward. Below are some basic examples:

### Example 1: Basic Hello World

```dart
void main() {
  print('Hello, Dart!');
}
```

### Example 2: Variables and Basic Operations

```
void main() {
  var name = 'Dart';
  var age = 10;
  print('Name: $name, Age: $age');
}

```

### Example 3: Using Comments

```
void main() {
  // This is a single-line comment
  /*
   This is a multi-line comment
  */
  print('Comments in Dart');
}

```

### Example 4: String Interpolation

```
void main() {
  var name = 'Dart';
  var message = 'Welcome to $name!';
  print(message);
}

```

### Example 5: Basic Function Declaration

```
void main() {
  greet('Dart');
}

void greet(String name) {
  print('Hello, $name!');
}

```

## Variables and Data Types

- Dart supports various data types such as integers, doubles, strings, and booleans.

### Example 1: Integer and Double

```
void main() {
  int a = 10;
  double b = 20.5;
  print('Integer: $a, Double: $b');
}

```
