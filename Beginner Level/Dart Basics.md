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

# Exercise

# Dart Programming Questions

## Syntax and Structure

### Objective Questions

1. **What is the purpose of the `main()` function in a Dart application?**

   - A) To initialize variables
   - B) To define the entry point of the application
   - C) To handle user input
   - D) To create classes

2. **Which of the following statements is correct about the `print()` function in Dart?**

   - A) It prints data to a file.
   - B) It outputs data to the console.
   - C) It creates a new variable.
   - D) It defines a new function.

3. **What does the `void` keyword signify in a Dart function?**

   - A) The function returns a value.
   - B) The function does not return a value.
   - C) The function is private.
   - D) The function is static.

4. **Which Dart construct is used to represent a block of code that is executed?**

   - A) Class
   - B) Function
   - C) Variable
   - D) Method

5. **How do you denote a single-line comment in Dart?**

   - A) `/* comment */`
   - B) `<!-- comment -->`
   - C) `// comment`
   - D) `# comment`

6. **Which of the following is NOT a valid identifier in Dart?**

   - A) `myVariable`
   - B) `_myVariable`
   - C) `2myVariable`
   - D) `myVariable2`

7. **How are multi-line comments written in Dart?**

   - A) `/* comment */`
   - B) `// comment //`
   - C) `<!-- comment -->`
   - D) `## comment ##`

8. **In Dart, what does the `main()` function need to have?**

   - A) A return type
   - B) A `void` return type
   - C) A parameter
   - D) A return statement

9. **What is the purpose of the `print()` function in Dart?**

   - A) To perform arithmetic operations
   - B) To print text to the console
   - C) To declare variables
   - D) To handle exceptions

10. **How do you include an external Dart file in another Dart file?**
    - A) `import 'filename.dart';`
    - B) `include 'filename.dart';`
    - C) `require 'filename.dart';`
    - D) `use 'filename.dart';`

### Subjective Questions

1. **Explain the role of the `main()` function in Dart and why it is important for Dart applications.**

2. **Describe how you would use the `print()` function to debug a Dart application. Provide an example.**

3. **Discuss the significance of comments in Dart and how they help in maintaining code quality.**

4. **Describe the syntax and purpose of Dart's multi-line comments. How do they differ from single-line comments?**

5. **Explain the importance of choosing meaningful identifiers in Dart code. How can poor naming conventions impact code readability?**

6. **Discuss how you would organize code into multiple files in a Dart project. What are the benefits of this approach?**

7. **What is the role of functions in Dart, and how do they contribute to code modularity and reusability?**

8. **How can you manage dependencies in a Dart project? Describe the role of `pubspec.yaml`.**

9. **What is a library in Dart, and how does it help in code organization? Provide an example of how to create and use a library.**

10. **Discuss the differences between Dart's `import` and `export` statements. How do they work together in code modularization?**

## Variables in Dart

### Objective Questions

1. **How can you declare a nullable variable in Dart?**

   - A) `int age = 25;`
   - B) `int? age = null;`
   - C) `final int age = 25;`
   - D) `const int age = 25;`

2. **Which keyword is used for declaring a variable whose type is inferred by Dart?**

   - A) `final`
   - B) `var`
   - C) `const`
   - D) `dynamic`

3. **What is the difference between `final` and `const` in Dart?**

   - A) `final` variables can be changed at runtime; `const` variables are compile-time constants.
   - B) `final` variables are compile-time constants; `const` variables can be changed at runtime.
   - C) Both `final` and `const` are compile-time constants.
   - D) Both `final` and `const` can be changed at runtime.

4. **What does the `var` keyword do in Dart?**

   - A) Defines a constant variable
   - B) Specifies the data type of the variable
   - C) Allows Dart to infer the type of the variable
   - D) Creates a variable with a fixed value

5. **How do you declare an implicitly typed variable in Dart?**

   - A) `var name = "Alice";`
   - B) `int name = "Alice";`
   - C) `final name = "Alice";`
   - D) `const name = "Alice";`

6. **What happens if you try to assign a null value to a non-nullable variable in Dart?**

   - A) The program will compile successfully.
   - B) The program will throw a runtime error.
   - C) The program will not compile.
   - D) The variable will be automatically converted to nullable.

7. **Which of the following statements is true about `final` variables in Dart?**

   - A) They can be assigned multiple times.
   - B) They can only be set once and cannot be changed after that.
   - C) They are compile-time constants.
   - D) They can be modified at runtime.

8. **How do you declare a constant value that is known at compile time in Dart?**

   - A) Using `final`
   - B) Using `var`
   - C) Using `const`
   - D) Using `dynamic`

9. **What is the main advantage of using `final` over `var` in Dart?**

   - A) `final` variables can be changed later; `var` variables cannot.
   - B) `final` variables can be set only once; `var` variables can be changed.
   - C) `final` variables are compile-time constants.
   - D) `var` variables are always nullable.

10. **How does Dart treat a variable declared with `const`?**
    - A) It allows runtime changes.
    - B) It creates a compile-time constant.
    - C) It defers initialization until runtime.
    - D) It allows null values.

### Subjective Questions

1. **Discuss the use of nullable variables in Dart. How do you declare and handle nullable variables?**

2. **Compare and contrast `final` and `const` in Dart. In what scenarios would you use each?**

3. **Explain how Dart’s type inference works when using the `var` keyword. Provide examples.**

4. **Describe the impact of making a variable `const` on its performance and memory usage.**

5. **How can the use of `final` and `const` contribute to code safety and reliability in Dart applications?**

6. **Discuss the implications of using non-nullable variables in Dart. How does this feature improve code robustness?**

7. **Explain how Dart handles variable initialization and the role of `late` keyword for deferred initialization.**

8. **What are some best practices for naming and organizing variables in Dart to ensure code clarity and maintainability?**

9. **Discuss the concept of type safety in Dart and how it relates to variable declaration and type inference.**

10. **How do Dart’s variable declaration and initialization mechanisms compare to those in other programming languages you are familiar with?**

## Data Types in Dart

### Objective Questions

1. **Which data type in Dart represents a sequence of characters?**

   - A) `int`
   - B) `double`
   - C) `String`
   - D) `bool`

2. **What is the purpose of the `num` type in Dart?**

   - A) To represent strings
   - B) To represent floating-point numbers
   - C) To represent both integers and floating-point numbers
   - D) To represent boolean values

3. **What is the default value of an uninitialized nullable variable in Dart?**

   - A) `0`
   - B) `false`
   - C) `null`
   - D) `""`

4. **Which data type would you use to represent a collection of unique items in Dart?**

   - A) `List`
   - B) `Map`
   - C) `Set`
   - D) `String`

5. **How does Dart treat strings in terms of mutability?**

   - A) Strings are mutable.
   - B) Strings are immutable.
   - C) Strings can be partially mutable.
   - D) Strings are mutable only if declared with `var`.

6. **Which data type is used to represent boolean values in Dart?**

   - A) `int`
   - B) `double`
   - C) `String`
   - D) `bool`

7. **What does the `dynamic` type in Dart allow you to do?**

   - A) Define a variable that can hold only integers
   - B) Create a variable that can change its type at runtime
   - C) Specify a compile-time constant
   - D) Represent a collection of key-value pairs

8. **What is the range of values for the `int` type in Dart?**

   - A) 0 to 1,000,000
   - B) -2^63 to 2^63 - 1
   - C) -2^31 to 2^31 - 1
   - D) -1,000,000 to 1,000,000

9. **Which type in Dart is used to represent a floating-point number?**

   - A) `int`
   - B) `num`
   - C) `String`
   - D) `bool`

10. **What will be the output of `print(5 ~/ 2);` in Dart?**
    - A) `2.5`
    - B) `2`
    - C) `3`
    - D) `2.0`

### Subjective Questions

1. **Discuss how Dart handles numeric types and their operations. Include examples for `int`, `double`, and `num`.**

2. **Explain the concept of immutability in Dart strings. Why might immutability be beneficial?**

3. **Describe how Dart's `dynamic` type can be used in situations where type flexibility is required. What are the potential risks associated with using `dynamic`?**

4. **Compare Dart’s `List` and `Set` types. When would you use one over the other? Provide examples.**

5. **Discuss the importance of type safety in Dart and how it relates to variables and data types.**

6. **Explain the use of `bool` in Dart and how boolean expressions are evaluated. Provide examples.**

7. **Describe how you can handle and convert between different numeric types in Dart.**

8. **Discuss how Dart’s type system helps prevent runtime errors and improves code reliability.**

9. **Explain how the `String` type in Dart can be manipulated and what methods are available for common string operations.**

10. **Describe the process of type inference in Dart and how it affects the declaration and usage of variables.**

## Basic Operators in Dart

### Objective Questions

1. **Which operator is used for integer division in Dart?**

   - A) `/`
   - B) `//`
   - C) `~/`
   - D) `%`

2. **What does the `&&` operator do in Dart?**

   - A) Adds two boolean values
   - B) Performs a bitwise AND operation
   - C) Returns true if both operands are true
   - D) Negates a boolean value

3. **Which operator is used for checking equality in Dart?**

   - A) `==`
   - B) `!=`
   - C) `>`
   - D) `<`

4. **What will the expression `5 % 2` return in Dart?**

   - A) `2.5`
   - B) `2`
   - C) `1`
   - D) `0`

5. **What does the `||` operator do in Dart?**

   - A) Performs a logical OR operation
   - B) Performs a bitwise OR operation
   - C) Performs a logical AND operation
   - D) Negates a boolean value

6. **Which operator is used to check if two values are not equal in Dart?**

   - A) `==`
   - B) `!=`
   - C) `>=`
   - D) `<=`

7. **What is the result of the expression `!true` in Dart?**

   - A) `true`
   - B) `false`
   - C) `null`
   - D) `0`

8. **Which operator is used for bitwise left shift in Dart?**

   - A) `<<`
   - B) `>>`
   - C) `&`
   - D) `|`

9. **What is the purpose of the `+=` operator in Dart?**

   - A) Assigns a value
   - B) Adds and assigns a value
   - C) Subtracts and assigns a value
   - D) Divides and assigns a value

10. **Which operator would you use to concatenate two strings in Dart?**
    - A) `+`
    - B) `&`
    - C) `|`
    - D) `*`

### Subjective Questions

1. **Describe how integer division and floating-point division differ in Dart. Provide examples using both operators.**

2. **Explain the difference between the `&&` and `||` logical operators in Dart. When would you use each?**

3. **Discuss the use of the `!` operator in Dart and how it affects boolean expressions. Provide an example.**

4. **Describe the bitwise operators available in Dart and provide examples of their usage.**

5. **Explain how the `+=` operator can simplify code when performing arithmetic operations. Provide an example.**

6. **Discuss the role of the modulo operator `%` in Dart. How can it be useful in programming?**

7. **Explain the concept of operator precedence in Dart and how it affects expression evaluation.**

8. **Describe how the `==` operator is used for comparing values in Dart. How does it differ from the `=` operator?**

9. **Discuss the use of the ternary operator `?:` in Dart. Provide an example of a ternary expression.**

10. **Explain how you can combine multiple operators in a single expression and how Dart evaluates such expressions.**
