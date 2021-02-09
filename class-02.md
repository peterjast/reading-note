[Table of Contents](https://peterjast.github.io/reading-notes/)

# **Text, CSS Introduction & Basic JS Instructions**

## Text

* Use HTML elements to structure page and provide semantic info: 
> Headings, paragraphs, bold, italic, superscript, subscript, line breaks, horizontal rule, strong, emphasis, quotations, abbreviations, acronyms, citations, definitions, author details, changes to content 
> h1, p, b, i, sup, sub, br, hr, strong, em, blockquote, q, abbr, cite, dfn, address, ins, del, s

## Cascadia Style Sheets Introductions

* CSS(Cascadia Style Sheets) can be used to control the design of your web page and make them more attractive
* CSS associates style rules with HTML elements using a **selector** and a **declaration**
    * The **selector** is the element the rule will apply to and the **declaration** 
    * **Declaration** describes the **property** that will be affected and specifies the display setting with a **value**   
* Version control is a system that allows you to store various versions of files as you change them.
* Storing various versions allows you to revert changes and to manage collaborative changes to a file or project.
* Using external style sheets allows you to use the same style rules for multiple pages, but they may also appear within an HTML page

### Selectors 

* UNIVERSAL
    > \* {}
* TYPE
    > h1, h2, h3 {}
* CLASS
    > .note {}
    > p.note {} 
* ID
    > #introduction {}
* CHILD
    > li>a {}
* DESCENDANT
    > p a {}
* ADJACENT SIBLING
    > h1+p {}  
* GENERAL SIBLING
    > h1~p {}    

## Basic JavaScript Instructions

*JavaScript gives a browser instructions to follow*

#### Statements 

*individual instructions*

> var today = new Date();
> var hourNow = today.getHours();
> var greeting;

#### Comments

*Write comments to explain what your code does*

> var today = new Date(); // Create a new date object
> var hourNow = today.getHours(); // Find the current hour  

#### Data Types

* NUMERIC
* STRING
* BOOLEAN

#### Arrays

*A special type of variable that stores a list of values*

> let colors;
> colors = ['green', 'blue', 'yellow'];
>
> let el = document.getElementById('colors');
> el.textContent = colors[0];

#### Expressions & Operators

##### An **expression** results in a single value

* Two types of expressions:

    * Assigning a value to a variable
    > var color = 'beige';

    * Expressions that use multiple values to return a single value
    > var area = 3 * 2;

##### Expressions use **operators** to create a single value 

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

