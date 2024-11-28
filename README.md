[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/SUHNlOlQ)

# Assignment - Functions

1.  What is a function?
    function is set of specific commands that can be called many times whenever you want and need.
2.  What is a function call?
    function call is when you call a function by its name.
3.  What is a code block, and how does it relate to a function?
    code block is line's of codes inside braces "{}" and it relates to function because it is the body of function.
4.  Create a function that takes a string as an argument and greets the user. For example, if the function is called with "John," the function should return "Hello, John!"

    ```javascript
    function greet(name) {
        return "Hello, " + name + "!";
    }
    ```

5.  Create a function that takes a string as an argument and returns a string with the argument value in reverse. For example, if the function is called with the input "hello," the function should return "olleh." (Use a loop, not a method that does this in one step.)

    ```javascript
    function reverseString(str) {
        let reversedStr = "";
        for (let i = str.length - 1; i >= 0; i--) {
            reversedStr += str[i];
        }
        return reversedStr;
    }
    ```

6.  What is a default argument, and how does it work?
    default argument is default value of function parameter,in case if there is no value passed to that parameter by user.
7.  What is the scope and lifetime of a variable?
    scope of variable is place where this variable is accessable,lifetime of variable is period of time using variable it starts from declaring variable and ends when stops using it,global variable exists while using app,local variable exists while using function.
8.  What is a return value?
    return value is value returned by function after function is executed
9.  What is the return value of a function that does not have a return statement?
    undefined
10. Given the following function, find mistakes in the code and explain what the function is supposed to do:

    ```javascript
    function foo(x) {
        x * 2; //correct way--"return x * 2" becaus function needs return statement  to return value,othervise it return value of undefined
    }

    let x = 7;
    x = foo(x);
    console.log(x);
    ```

11. Given the following code, find and correct the mistake in the code:

    ```javascript
    function bar() {
        //while calling this function arguments wasnt passed so it will not change global variable x ,it will change default parameter of x,to correct mistake we can just remove parameter from this function and it will effect global x.
        x += 1;
    }

    function foo() {
        bar(); //calling function but not passing any argument
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
    function foo(x) { //2 is not greater than 5 so it will return 2 + foo(2+1) that means it will call function again
    if (2 > 5) {
    return 2;
    } else {
    return 2 + foo(2 + 1);
    }
    }
    function foo(x) { //3 is not greater than 5 so it will return 3 + foo(3+1) that means it will call function again
    if (3 > 5) {
    return 3;
    } else {
    return 3 + foo(3 + 1);
    }
    }
    function foo(x) { //4 is not greater than 5 so it will return 4 + foo(4+1) that means it will call function again
    if (4 > 5) {
    return 4;
    } else {
    return 4 + foo(4 + 1);
    }
    }
    function foo(x) { //5 is not greater than 5 so it will return 5 + foo(5+1) that means it will call function again
    if (5 > 5) {
    return 5;
    } else {
    return 5 + foo(5 + 1);
    }
    }
    function foo(x) { // 6 is greater than 5 so it will return 6 and stops there.but while calling function again and again it will summ all return's (2 + foo(2+1) + 3 + foo(3+1) + 4 + foo(4+1) + 5 + foo(5+1) + 6) 2+3+4+5+6 = 20
    if (6 > 5) {
    return 6;
    } else {
    return 6 + foo(6 + 1);
    }
    }
13. Create a function that takes an array of numbers as an argument and returns the sum of the odd numbers in the array. (Use a loop, not a method that does this in one step.)

```javascript
let array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14];
function sumOddNumbers(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] % 2 == 0) {
            sum += arr[i];
        }
    }
    return sum;
}
```

14. Create a function that takes a string as an argument and returns a boolean, true if string is a palindrome else false. A palindrome is a word that reads the same backward as forward. For example, if the function is called with `"hello"` it should return `false`, if the function receives `"elle"` it should return `true`, because `elle` backwards is also `elle`.

```javascript
function isPalindrome(str) {
    let strArray = [];
    let reverseStrArrayToString = "";
    //string to array
    for (let i = 0; i < str.length; i++) {
        strArray[i] = str[i];
    }
    //array to string,reverse version
    for (let i = strArray.length - 1; i >= 0; i--) {
        reverseStrArrayToString += strArray[i];
    }
    if (str === reverseStrArrayToString) {
        return true;
    }
    return false;
}
```
