[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/SUHNlOlQ)
# Assignment - Functions

1. What is a function?
2. What is a function call?
3. What is a code block, and how does it relate to a function?
4. Create a function that takes a string as an argument and greets the user. For example, if the function is called with "John," the function should return "Hello, John!"
5. Create a function that takes a string as an argument and returns a string with the argument value in reverse. For example, if the function is called with the input "hello," the function should return "olleh." (Use a loop, not a method that does this in one step.)
6. What is a default argument, and how does it work?
7. What is the scope and lifetime of a variable?
8. What is a return value?
9. What is the return value of a function that does not have a return statement?
10. Given the following function, find mistakes in the code and explain what the function is supposed to do:
    ```javascript
    function foo(x) {
        x * 2;
    }
    
    let x = 7;
    x = foo(x);
    console.log(x);
    ```
11. Given the following code, find and correct the mistake in the code:
    ```javascript
    function bar(x = 8) {
        x += 1;
    }

    function foo() {
        bar();
        x *= 2;
    }
    
    let x = 7;
    foo(x);
    console.log(x); // x should change!
    ```
12. Given the following function, what is the return value of the function call `foo(2)`? Explain your answer.
    ```javascript
    function foo(x) {
        if (x > 5) {
            return x;
        } else {
            return x + foo(x + 1);
        }
    }
    ```
13. Create a function that takes an array of numbers as an argument and returns the sum of the odd numbers in the array. (Use a loop, not a method that does this in one step.)
14. Create a function that takes a string as an argument and returns a boolean, true if string is a palindrome else false. A palindrome is a word that reads the same backward as forward. For example, if the function is called with `"hello"` it should return `false`, if the function receives `"elle"` it should return `true`, because `elle` backwards is also `elle`.
