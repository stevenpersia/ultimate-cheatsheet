
# Conditional Statements

The conditional statements in JavaScript help make decisions easier based on certain conditions. The condition specified in the statement can be either true or false. The code with the conditional statements executes if true. 
There are 4 types of conditional statements:

## if statement 

An if statement executes a specified code segment if the given condition is ''true.''

```js
var age = 12;
//condition 
if (age>= 0 && age<= 14) {
    //if condition is met
    AgeCategories = "Children";
}
```
----
## else statement 

An else statement executes the code associated with the else if the given if condition is ''false.''

```js
var age = 22;
//condition 
if (age>= 0 && age<= 14) {
    
    AgeCategories = "Children";
} else {
    //if condition is not met
    AgeCategories = "Not a Child anymore.";
}
```
----
## else if statement 

An else if statement specifies a new condition for testing when the first if condition is ''false.''

```js
var age = 22;
//condition 
if (age>= 0 && age<= 14) {
    
    AgeCategories = "Children";
} else if (age>= 15 && age<= 24) {
    //if 2nd condition is met
    AgeCategories = "Youth";

} else {

    AgeCategories = "Not a Child or Youth anymore.";
}
```
----
## switch-case statement 

A switch-case statement specifies multiple alternative code blocks for execution and executes these cases based on certain conditions.

```js
//Students grade input
var grade = 'B';

switch(grade) {
    case 'A':
        result = "Grade: A";
    break;
    case 'B': //this will meet the condition 
        result = "Grade: B"; // This will print out
    break;
    case 'C':
        result = "Grade: C";
    break;
    case 'D':
        result = "Grade: D";
    break;
    default:
        result="No Grade";
}

```
----