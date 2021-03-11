[Table of Contents](https://peterjast.github.io/reading-notes/)

# **Programming with Javascript**

## Important Concepts

* JavaScript is used in browsers to make web pages dynamic, interactive and interesting
* JavaScript can be used to: 
    * Access content
    * Modify content
    * Program rules 
    * React to events

* A script is a series of instructions
* To write a script:
    1. Define the goal
    1. Design the script
    1. Code each step
    

### Expressions & Operators

#### An **expression** results in a single value

* Two types of expressions:

    * Assigning a value to a variable
    > var color = 'beige';

    * Expressions that use multiple values to return a single value
    > var area = 3 * 2;

#### Expressions use **operators** to create a single value 

* Types of operators:

    * Assignment
    > color = 'beige';
    
    * Arithmetic
    > area = 3 * 2;
    > /+ - / * ++ -- %

    * String
    > greeting = 'Hi' + 'Molly';

    * Comparison
    > buy = 3 > 5;

    * Logical
    > buy = (5 > 3) && (2 < 4);

### Functions
  
*Functions are a series of statements grouped together to perform a task*

#### Declaring a function using function keyword, function name and code block in curly braces:

> function sayHello() {
>    document.write('Hello');
> }

#### Calling a function:

> sayHello();

#### Declaring functions with **parameters**:

> function getArea(width, height) {
>    return width * height;
> }

#### Calling functions with **arguments**:

Arguments as values:

> getArea(3,5);

Arguments as variables:

> wallWidth = 3;
> wallHeight = 5;
> getArea(wallWidth, wallHeight);

#### Getting a single value from a function

> function calculateArea(width, height) {
>   var area = width * height;
>   return area;    
> }
> var wallOne = calculateArea(3, 5);
> var wallTwo = calculateArea(8, 5);