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
