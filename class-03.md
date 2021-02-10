[Table of Contents](https://peterjast.github.io/reading-notes/)

# **HTML Lists, Control Flow with JS, and the CSS Box Model**

## Lists

### 3 types of HTML lists

    * ORDERED - ordered lists are numbered 
    > ol - ordered list
    > li - list item
    
    * UNORDERED - use bullet points
    > ul - unordered list
    > li - list item

    * DEFINITION - define terms
    > dl - definition list
    > dt - definition term
    > dd - definition description

    *lists can be nested*

## CSS Box Model

* HTML elements are treated as boxes by CSS
* Use CSS to control dimensions, borders, margins, and padding for each box
* Use display and visibility properties to hide elements
* You can change whether a box is inline or a block-level
* You can create border images and rounded borders

## Basic JS Instructions - Arrays

* An array variable stores a list of values that are related to eachother

### ARRAY LITERAL

    > let names;
    > names = ['John', 'James', 'Jason']
    >
    > let el = document.getElementById('names');
    > el.textContent = names[0];

### ARRAY CONTRUCTOR

    > let names = new Array('John',
    >                       'James',    
    >                       'Jason');
    >
    > let el = document.getElementById('names');
    > el.textContent = names[0];

*array literal is preferred*        

### ACCESSING ARRAY ITEMS

    > let nameThree;
    > nameThree = names[2];

### NUMBER OF ARRAY ITEMS

    > let numNames;
    > let names.length

### CHANGING VALUES IN AN ARRAY

    > names[2] = 'Jenny';

## JS Decisions and Loops 

### IF...ELSE STATEMENTS

    > if (score >= 10) {
    >   win();
    > }
    > else {
    >   lose();
    > }

### LOOPS

Loops check a condition. If the condition returns true, a code block will run until the condition returns false.

There are 3 types of loops:

#### FOR LOOP

    > for (var i = 0; i < 10; i++) {
    >   document.write(i);
    > }

##### INITIALIZATION

    > var i = 0;

##### CONDITION

    > i < 10;

##### UPDATE

    > i++

#### WHILE LOOP

Use a while loop when you do not know how many times you want to run the code.

    > var i = 1;
    > var msg = '';
    >
    > while (i < 10) {
    >    msg += i + ' x5 = ' + (i * 5) + '<br />;
    >    i++;
    > }
    >
    > document.getElementById('answer').innerHTML = msg;

#### DO WHILE

Use a do while loop when you want the code to run at least once regardless of whether or not the condition is met.

    > var i = 1;
    > var msg = '';
    >
    > do {
    >   msg += i + ' x5 = ' + (i * 5) + '<br />;
    >   i++;
    > } while (i < 1);
    >
    > document.getElementById('answer').innerHTML = msg;