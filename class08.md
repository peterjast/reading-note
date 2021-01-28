[Table of Contents](https://peterjast.github.io/reading-notes/)

# **Operators & Loops**

## Comparison Operators

Comparing values using operators will return true or false

* IS EQUAL TO

> ==

* IS NOT EQUAL TO

> !=

* STRICT EQUAL TO

> ===

* STRICT NOT EQUAL TO

> !==

* GREATER THAN 

> \>

* LESS THAN

> <

* GREATER THAN OR EQUAL TO

> \>=

* LESS THAN OR EQUAL TO

> <=

## Logical Operators

Compare results of more than one comparison operator using logical operators

> ((5 < 2>) && (2 >= 3))

* LOGICAL AND

> &&

* LOGICAL OR

> ||

* LOGICAL NOT

> !

## loops

Loops check a condition. If the condition returns true, a code block will run until the condition returns false.

There are 3 types of loops:

#### FOR LOOP

> for (var i = 0; i < 10; i++) {
    document.write(i);
}

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

