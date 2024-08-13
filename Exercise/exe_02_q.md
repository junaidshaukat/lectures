# Control Flow in Dart: `if`, `else if`, and `else` Statements

## Objective Questions

1. **What is the purpose of the `if` statement in Dart?**

   - a) To check if a condition is false
   - b) To execute a block of code if a condition is true
   - c) To execute a block of code if a condition is false
   - d) To terminate a loop

2. **Which statement is used to execute a block of code when the `if` condition is false?**

   - a) `elseif`
   - b) `break`
   - c) `else`
   - d) `continue`

3. **How many `else` blocks can be used with a single `if` statement?**

   - a) One
   - b) Two
   - c) Unlimited
   - d) None

4. **Which of the following is the correct syntax for an `if` statement?**

   - a) `if condition {}`
   - b) `if (condition) {}`
   - c) `if (condition) []`
   - d) `if condition []`

5. **What will be the output of the following code?**

   ```dart
   int x = 20;
   if (x < 15) {
     print("Less than 15");
   } else {
     print("15 or more");
   }
   ```

   - a) Less than 15
   - b) 15 or more
   - c) 20
   - d) No output

6. **Which statement is used to check multiple conditions sequentially?**

   - a) else
   - b) else if
   - c) switch
   - d) continue

7. **What is the output of the following code?**

   ```dart
    int number = -5;
    if (number > 0) {
      print('Positive');
    } else if (number < 0) {
      print('Negative');
    } else {
      print('Zero');
    }
   ```

   - a) Positive
   - b) Negative
   - c) Zero
   - d) No output

8. **Can multiple `else if` blocks be used in a single `if-else` structure?**

   - a) Yes
   - b) No

9. **Which keyword is used to execute an alternative block of code if all if and else if conditions are false?**

   - a) final
   - b) else
   - c) break
   - d) return

10. **What will happen if all conditions in an if-else if structure are false and there is no else block?**

    - a) The program will crash
    - b) A default action is executed
    - c) No code will be executed in that block
    - d) The last else if block will be executed

11. **Which statement about if statements is true?**

    - a) if statements cannot be nested
    - b) if statements can only have one condition
    - c) if statements can be used without else or else if
    - d) if statements must always be followed by else

12. **What does the following code print?**

    ```dart
      int a = 10;
      int b = 20;
      if (a == b) {
        print('Equal');
      } else {
        print('Not Equal');
      }
    ```

    - a) Equal
    - b) Not Equal
    - c) 10
    - d) 20

13. **Which of the following is a valid condition in an if statement?**

    - a) if (true)
    - b) if (5)
    - c) if ('true')
    - d) if ([1, 2, 3])

14. **What is the output of the following code?**
    ```dart
    int age = 25;
    if (age > 18) {
      print('Adult');
    } else {
      print('Minor');
    }
    ```
    - a) Adult
    - b) Minor
    - c) 25
    - d) No output
15. **Is it possible to have an if statement without any else or else if?**

    - a) Yes
    - b) No

## Subjective Questions

1. **Explain the use of the if statement in Dart with an example.**

2. **Describe how the else statement works in a control flow structure.**

3. **What is the difference between else and else if in Dart? Provide examples.**

4. **How does Dart handle multiple conditions using else if? Illustrate with code.**

5. **Write a Dart program that prints "High" if a number is greater than 100, "Medium" if it's between 50 and 100, and "Low" if it's less than 50.**

6. **Explain what happens when none of the conditions in an if-else if structure are true, and there's no else block.**

7. **Can if, else if, and else statements be nested? Provide an example.**

8. **What are the limitations of using only if and else without else if?**

9. **Discuss the importance of the order of conditions in an if-else if structure.**

10. **Write a Dart program that categorizes a number as positive, negative, or zero using if, else if, and else statements.**

11. **How would you modify an if-else if structure to handle more complex conditions?**

12. **Explain the role of Boolean expressions in if statements with an example.**

13. **What is the significance of the else block in control flow, and how does it improve code readability?**

14. **Describe a scenario where you would use multiple else if statements instead of just if and else.**

15. **Write a Dart program that checks if a year is a leap year or not using if, else if, and else statements.**
