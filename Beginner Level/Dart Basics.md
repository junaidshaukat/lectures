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

```dart
void main() {
  // Entry point of the application
  print('Hello, Dart!');
}
```

- main(): The entry point of every Dart application.
- print(): A built-in function to output data to the console.

# Variables in Dart

In Dart, variables are used to store data that can be used and manipulated throughout the program. A variable has a name (also called an identifier) and a type, which determines the kind of data it can hold.

## 1. Declaring Variables

- You can declare a variable by specifying its type followed by its name.
- Variables can be declared with or without an initial value.

## 2. Types of Variables

- **Explicitly Typed Variables:** You can declare a variable with a specific type, such as `int`, `double`, `String`, `bool`, or any custom class.
- **Implicitly Typed Variables:** You can declare a variable using the `var` keyword, and Dart will infer its type based on the initial value.
- **Nullable Variables:** By default, variables in Dart are non-nullable (cannot hold a `null` value). You can make a variable nullable by appending a question mark `?` to its type.

## 3. Final and Const

- **`final`:** A variable declared with `final` can be set only once. After it is set, it cannot be changed.
- **`const`:** A variable declared with `const` is a compile-time constant. The value must be known at compile time and cannot be changed afterward.

## Examples

### Example 1: Explicitly Typed Variables

```dart
void main() {
  int age = 30;  // Explicitly typed integer variable
  double height = 5.9;  // Explicitly typed double variable
  String name = "John";  // Explicitly typed string variable
  bool isStudent = true;  // Explicitly typed boolean variable

  print("Name: $name, Age: $age, Height: $height, Student: $isStudent");
}
```

### Example 2: Implicitly Typed Variables

```dart
void main() {
  var age = 30;  // Dart infers the type as int
  var height = 5.9;  // Dart infers the type as double
  var name = "John";  // Dart infers the type as String
  var isStudent = true;  // Dart infers the type as bool

  print("Name: $name, Age: $age, Height: $height, Student: $isStudent");
}

```

### Example 3: Nullable Variables

```dart
void main() {
    int? age = null; // Nullable integer variable
    String? name; // Nullable string variable (defaults to null)
    age = 25; // Assigning a value later
    name = "Alice";
    print("Name: $name, Age: $age");
}

```

### Example 4: Final and Const

```dart
void main() {
  final int age = 30;  // Can only be set once
  const double pi = 3.14159;  // Compile-time constant

  // age = 35; // Error: Cannot change the value of a final variable
  // pi = 3.14; // Error: Cannot change the value of a const variable

  print("Age: $age, Pi: $pi");
}

```

# Data Types in Dart

Dart is a statically typed language, which means that every variable you define has a type, and this type must be known at compile time. Dart provides a variety of built-in data types to handle different kinds of data.

## 1. Basic Data Types

### 1.1. Numbers

- **`int`**: Represents whole numbers without a decimal point.
  - Example: `int age = 30;`
- **`double`**: Represents floating-point numbers, which can have a decimal point.
  - Example: `double height = 5.9;`
- **`num`**: A superclass of `int` and `double` that can represent both.
  - Example: `num value = 42;` // Can be assigned `int`.
  - Example: `num value = 42.5;` // Can be assigned `double`.

### 1.2. Strings

- **`String`**: Represents a sequence of characters (text).
  - Example: `String name = "Alice";`
- Strings are immutable, meaning their content cannot be changed after creation. You can use single or double quotes, and you can also use triple quotes for multi-line strings.
  - Example: `String greeting = '''Hello, World!''';`

### 1.3. Booleans

- **`bool`**: Represents a value that is either `true` or `false`.
  - Example: `bool isVisible = true;`

### 1.4. Lists

- **`List`**: An ordered collection of objects, also known as an array.
  - Example: `List<int> numbers = [1, 2, 3, 4, 5];`
- Lists can be fixed-length or growable, and they can contain objects of any type.

### 1.5. Maps

- **`Map`**: A collection of key-value pairs. Keys are unique, and each key is associated with one value.
  - Example: `Map<String, int> scores = {"Alice": 95, "Bob": 85};`

### 1.6. Sets

- **`Set`**: An unordered collection of unique items.
  - Example: `Set<int> uniqueNumbers = {1, 2, 3};`
- Sets are useful when you need to store a collection of unique items without duplicates.

### 1.7. Runes and Symbols

- **`Runes`**: Represents Unicode characters in a string. Useful for handling special characters.
  - Example: `Runes heart = Runes('\u2665');`
- **`Symbol`**: Used to refer to identifiers by name.
  - Example: `Symbol sym = #mySymbol;`

## 2. Special Data Types

### 2.1. Null

- **`Null`**: Represents the absence of a value. In Dart, variables of type `Null` can only have the value `null`.
  - Example: `Null n = null;`

### 2.2. Dynamic

- **`dynamic`**: A special type that disables type checking for a variable. The type of a `dynamic` variable can change during runtime.
  - Example: `dynamic variable = 42;` // Can later be assigned a string.

### 2.3. Object

- **`Object`**: The root of the Dart class hierarchy. All Dart classes inherit from `Object`.
  - Example: `Object obj = "Hello";` // Can hold any data type.

## 3. Type Conversions

Dart provides several methods for type conversions, such as `toString()`, `toInt()`, and `toDouble()`.

- Example:
  ```dart
  int num = 10;
  String str = num.toString();  // Converts int to String
  ```

## 4. Example Usage

```dart
void main() {
  // Numbers
  int age = 25;
  double height = 5.9;
  num weight = 70.5;

  // Strings
  String name = "John";
  String address = '''1234 Elm Street
                      Springfield, USA''';

  // Booleans
  bool isActive = true;

  // Lists
  List<String> fruits = ["Apple", "Banana", "Mango"];

  // Maps
  Map<String, int> scores = {"Alice": 95, "Bob": 85};

  // Sets
  Set<int> uniqueIds = {1, 2, 3};

  // Runes
  Runes heart = Runes('\u2665');

  // Dynamic
  dynamic variable = "Hello"; // Can change to any type

  // Object
  Object obj = 42;

  print("Name: $name, Age: $age, Height: $height, Active: $isActive");
}
```

# Basic Operators in Dart

Dart provides a wide range of operators to perform various operations on data. These operators can be grouped into different categories based on their functionality.

## 1. Arithmetic Operators

These operators are used to perform basic arithmetic operations.

- **`+`** (Addition): Adds two operands.
  - Example: `int sum = 5 + 3;  // sum is 8`
- **`-`** (Subtraction): Subtracts the second operand from the first.
  - Example: `int difference = 5 - 3;  // difference is 2`
- **`*`** (Multiplication): Multiplies two operands.
  - Example: `int product = 5 * 3;  // product is 15`
- **`/`** (Division): Divides the first operand by the second. The result is a double.
  - Example: `double quotient = 5 / 2;  // quotient is 2.5`
- **`~/`** (Integer Division): Divides the first operand by the second and returns an integer.
  - Example: `int quotient = 5 ~/ 2;  // quotient is 2`
- **`%`** (Modulus): Returns the remainder of the division.
  - Example: `int remainder = 5 % 2;  // remainder is 1`

## 2. Relational (Comparison) Operators

These operators are used to compare two values and return a boolean result (`true` or `false`).

- **`==`** (Equal to): Returns `true` if the operands are equal.
  - Example: `bool isEqual = (5 == 3);  // isEqual is false`
- **`!=`** (Not equal to): Returns `true` if the operands are not equal.
  - Example: `bool isNotEqual = (5 != 3);  // isNotEqual is true`
- **`>`** (Greater than): Returns `true` if the left operand is greater than the right.
  - Example: `bool isGreater = (5 > 3);  // isGreater is true`
- **`<`** (Less than): Returns `true` if the left operand is less than the right.
  - Example: `bool isLess = (5 < 3);  // isLess is false`
- **`>=`** (Greater than or equal to): Returns `true` if the left operand is greater than or equal to the right.
  - Example: `bool isGreaterOrEqual = (5 >= 3);  // isGreaterOrEqual is true`
- **`<=`** (Less than or equal to): Returns `true` if the left operand is less than or equal to the right.
  - Example: `bool isLessOrEqual = (5 <= 3);  // isLessOrEqual is false`

## 3. Logical Operators

These operators are used to combine multiple boolean expressions.

- **`&&`** (Logical AND): Returns `true` if both operands are true.
  - Example: `bool result = (5 > 3) && (2 < 4);  // result is true`
- **`||`** (Logical OR): Returns `true` if at least one of the operands is true.
  - Example: `bool result = (5 > 3) || (2 > 4);  // result is true`
- **`!`** (Logical NOT): Reverses the boolean value of its operand.
  - Example: `bool result = !(5 > 3);  // result is false`

## 4. Assignment Operators

These operators are used to assign values to variables.

- **`=`** (Assignment): Assigns the right operand to the left operand.
  - Example: `int a = 5;  // a is 5`
- **`+=`** (Add and assign): Adds the right operand to the left operand and assigns the result to the left operand.
  - Example: `a += 3;  // a is now 8`
- **`-=`** (Subtract and assign): Subtracts the right operand from the left operand and assigns the result to the left operand.
  - Example: `a -= 2;  // a is now 6`
- **`*=`** (Multiply and assign): Multiplies the left operand by the right operand and assigns the result to the left operand.
  - Example: `a *= 2;  // a is now 12`
- **`/=`** (Divide and assign): Divides the left operand by the right operand and assigns the result to the left operand.
  - Example: `a /= 3;  // a is now 4.0`
- **`%=`** (Modulus and assign): Takes the modulus of the left operand by the right operand and assigns the result to the left operand.
  - Example: `a %= 2;  // a is now 0`

## 5. Unary Operators

These operators operate on a single operand.

- **`++`** (Increment): Increases the value of the operand by 1.
  - Example: `int a = 5; a++;  // a is now 6`
- **`--`** (Decrement): Decreases the value of the operand by 1.
  - Example: `int a = 5; a--;  // a is now 4`
- **`-`** (Unary minus): Changes the sign of the operand.
  - Example: `int a = 5; int b = -a;  // b is -5`
- **`!`** (Logical NOT): Reverses the boolean value of the operand.
  - Example: `bool a = true; bool b = !a;  // b is false`

## 6. Bitwise Operators

These operators are used to perform bit-level operations on integers.

- **`&`** (Bitwise AND): Performs a bitwise AND operation on two integers.
  - Example: `int result = 5 & 3;  // result is 1`
- **`|`** (Bitwise OR): Performs a bitwise OR operation on two integers.
  - Example: `int result = 5 | 3;  // result is 7`
- **`^`** (Bitwise XOR): Performs a bitwise XOR operation on two integers.
  - Example: `int result = 5 ^ 3;  // result is 6`
- **`~`** (Bitwise NOT): Inverts all the bits of the operand.
  - Example: `int result = ~5;  // result is -6`
- **`<<`** (Left shift): Shifts the bits of the first operand left by the number of positions specified by the second operand.
  - Example: `int result = 5 << 1;  // result is 10`
- **`>>`** (Right shift): Shifts the bits of the first operand right by the number of positions specified by the second operand.
  - Example: `int result = 5 >> 1;  // result is 2`

## 7. Conditional Operators

These operators are used to evaluate expressions based on a condition.

- **`?:`** (Ternary Operator): Evaluates a condition and returns one of two values.
  - Example: `int a = 5; int b = 3; int result = (a > b) ? a : b;  // result is 5`
- **`??`** (Null-aware Operator): Returns the left operand if it is not null, otherwise returns the right operand.
  - Example: `String name = null; String result = name ?? "Guest";  // result is "Guest"`

## 8. Type Test Operators

These operators are used to check the type of an object at runtime.

- **`is`**: Checks if the object is of a specific type.
  - Example: `if (name is String) { /* Do something */ }`
- **`is!`**: Checks if the object is not of a specific type.
  - Example: `if (name is! String) { /* Do something */ }`

## 9. Cascade Notation (..) Operator

This operator is used to perform a sequence of operations on the same object.

- **`..`**: Allows you to call multiple methods on the same object.
  - Example:
    ```dart
    var buffer = StringBuffer()
      ..write("Hello")
      ..write(" World")
      ..write("!");
    ```

## 10. Example Usage

```dart
void main() {
  // Arithmetic Operators
  int a = 10;
  int b = 3;
  print(a + b);  // 13
  print(a - b);  // 7
  print(a * b);  // 30
  print(a / b);  // 3.3333333333333335
  print(a % b);  // 1

  // Relational Operators
  print(a > b);  // true
  print(a < b);  // false

  // Logical Operators
  bool isTrue = true;
  bool isFalse = false;
  print(isTrue && isFalse);  // false
  print(isTrue || isFalse);  // true

  // Assignment Operators
  int c = 5;
  c += 2;  // c = c + 2
  print(c);  // 7

  // Unary Operators
  int d = 10;
  d++;  // d = d + 1
  print(d);  // 11

  // Bitwise Operators
  int e = 5;  // 0101
  int f = 3;  // 0011
  print(e & f);  // 1 (0001)
  print(e | f);  // 7 (0111)

  // Conditional Operators
  String name = "Alice";
  String greeting = (name == "Alice") ? "Hello, Alice!" : "Who are you?";
  print(greeting);  // Hello, Alice!

  // Type Test Operators
  if (name is String) {
    print("Name is a String");
  }

  // Cascade Notation
  var sb = StringBuffer()
    ..write("Dart")
    ..write(" is")
    ..write(" awesome!");
  print(sb.toString());  // Dart is awesome!
}
```

## Control Flow

Control flow in Dart refers to how the execution of code is directed based on different conditions and structures. Dart, like many other programming languages, provides various control flow constructs, including conditional statements, loops, and exception handling.

# Control Flow in Dart: `if`, `else if`, and `else` Statements

## Overview

The `if`, `else if`, and `else` statements are fundamental control flow structures in Dart, used to execute different blocks of code based on specific conditions. These statements evaluate Boolean expressions and execute code depending on whether the expressions are `true` or `false`.

## `if` Statement

The `if` statement is used to test a condition. If the condition evaluates to `true`, the code block inside the `if` statement is executed.

### Syntax

```dart
if (condition) {
  // code to be executed if condition is true
}
```

### Example

```dart
void main() {
  int number = 10;

  if (number > 5) {
    print('The number is greater than 5');
  }
}
```

### Explanation

The condition number > 5 is checked.
Since 10 is greater than 5, the condition is true, and the message "The number is greater than 5" is printed.

## `else` Statement

The else statement executes a block of code if the condition in the if statement is false. It provides an alternative code path when the if condition fails.

### Syntax

```dart
if (condition) {
  // code to be executed if condition is true
} else {
  // code to be executed if condition is false
}
```

### Example

```dart
void main() {
  int number = 3;

  if (number > 5) {
    print('The number is greater than 5');
  } else {
    print('The number is 5 or less');
  }
}
```

### Explanation

The condition number > 5 is checked.
Since 3 is not greater than 5, the condition is false, and the message "The number is 5 or less" is printed.

## `else if` Statement

The else if statement allows you to check multiple conditions sequentially. If the if condition is false, the else if condition is evaluated. Multiple else if statements can be used to test various conditions. If none of the conditions are true, the else block (if provided) is executed.

### Syntax

```dart
if (condition1) {
  // code to be executed if condition1 is true
} else if (condition2) {
  // code to be executed if condition1 is false and condition2 is true
} else if (condition3) {
  // code to be executed if condition1 and condition2 are false and condition3 is true
} else {
  // code to be executed if all conditions are false
}
```

### Example

```dart
void main() {
  int number = 0;

  if (number > 0) {
    print('The number is positive');
  } else if (number < 0) {
    print('The number is negative');
  } else {
    print('The number is zero');
  }
}
```

### Explanation

First, the condition number > 0 is checked. Since 0 is not greater than 0, this condition is false.

Then, the condition number < 0 is checked. Since 0 is not less than 0, this condition is also false.

Finally, since neither of the above conditions is true, the else block is executed, and the message "The number is zero" is printed.

# Exercise
