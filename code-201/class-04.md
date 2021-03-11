[Table of Contents](https://peterjast.github.io/reading-notes/)

# **HTML Links, JS Functions, and Intro to CSS Layout**

## HTML Links

Links allow you to move from one page to another

### Common Types of Links

* one website to another

* page to page on same website

* one part of a page to another part of same page

* links that open in new browser window or new tab

* links that open an email addressed to someone

### Writing Links

#### Write links using the <a> element

    > <a href="http://www.imdb.com">IMDB</a>

## CSS Layout

* elements group together sections of a page

* browsers will display pages with normal flow, but relative, absolute or fixed posititioning can be specified

* float property moves content to left or right of page

* float can be used to create columns

* pages can have a liquid or fixed layout

* keep pages within 960-1000 pixels wide and main concepts in top 600 pixels

* use grids for professional and flexible designs

* CSS Frameworks make styling your page easier by providing rules for common tasks

* multiple CSS files can be included in one page

## Functions, Methods and Objects

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

#### Variable Scope

* where you declare a variable changes where it can be used:
  
  * global scope
  
  * local scope
