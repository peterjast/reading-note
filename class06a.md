[Table of Contents](https://peterjast.github.io/reading-notes/)

# **Dynamic web pages with Javascript**

## Important Concepts

* HTML, CSS and JavaScript are each important layers for creating dynamic web pages
    * HTML is the content layer
    * CSS is the presentation layer
    * Javascript is the behavior layer
* JS is written in plain text 
* A JS file uses the .js extension
* JS runs where it is found in the HTML
* The **script** element tells the browser to load the JavaScript file

### Using Objects & Methods

* The **document** object represents entire web page and the **write()** method allows new content to load where the **script** element is in the HTML
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

  
