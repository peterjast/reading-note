[Table of Contents](https://peterjast.github.io/reading-notes/)

# **HTML & Javascript**

## Important Concepts

* HTML, CSS and JavaScript are each important layers for creating dynamic web pages
    * HTML is the content layer
    * CSS is the presentation layer
    * Javascript is the behavior layer
* JS is written in plain text 
* A JS file uses the .js extension
* JS runs where it is found in the HTML
* The **script** element tells the browser to load the JavaScript file

### HTML & Extra Markup

* Write comments in HTML
* The meta element lives inside the head element 
* Meta data is information about the web page such as description, keywords, robots, author, pragma and expires
* Some characters are reserved for HTML code, so you need to use escape characters if you want them to appear on your website
* HTML5 layouts introduce new elements to divide parts of your web page such as header, article, footer, nav, figure, etc.

#### Structure

* HTML(Hypertext Markup Language) pages are text documents that create the structure of web pages
* HTML uses elements structure the page 
* Elements have an opening tag and a closing tag
* Attributes give more information about elements 
* Attributes require a name and value


#### Process & Design

* When designing a website, consider the target audience and what information they would expect to find.

    * Create imaginary users to help dictate the design of your website
    * Who will be visiting your website?
    * What is the motication for visiting your website?
    * What specific goal are they trying to achieve by visiting your website?
    * What information do your visitors need?
    * What are the most important features?
    * How often are people visiting your site and how often do you need to update information?

* Once you know what information you need to appear on your site, you can organize it into sections or pages using a **site map**. 

    * A **site map** is a diagram of the structure of your site
    * You decide how to group information for each page
    * You can use **card sorting** to organize information for each page
    * Organize groups of information to create a flow for how users will navigate your page
    

* Use a **wireframe** to sketch out the design of your site.

    * A **wireframe** is a sketch of the layout of your site
    * It shows the hierarchy of information
    * Shows you how much space each page and section might require
    * Gives you a guide for when you start to code your page

* Use your design to get your message across

    * The goal of a visual design is to communicate
    * Websites have a lot of information to communicate
    * The design shows what information is important
    * Shows users what order to read information
    * Controls the flow of your site
    * A visual heirarchy shows what information should be prioritized
    * Size, color and style control the visual hierarchy - the order in which information is perceived
    * Organization groups blocks of related content together and makes it easier to understand
    * Grouping and similarity helps your page appear organized and easy to understand

* When designing your navigation, consider the following:
    * concise
    * clear
    * selective
    * context
    * interactive
    * consistent    

#### Layouts

* The new HTML5 elements help structure a website 
* They provide clearer code than using multiple div elements
    * header
    * footer
    * nav
    * article
    * aside
    * section
    * hgroup
    * figure
* Some methods require parameters
  > $ document.write('Good afternoon!');
  > <script src="js/add-content.js"></script>

### Basic JavaScript Instructions
  
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

#### Functions
  
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