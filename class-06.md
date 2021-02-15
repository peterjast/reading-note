[Table of Contents](https://peterjast.github.io/reading-notes/)

# **Problem Domain, Objects, and the DOM**

## Problem Domain

According to John Sonmez, the hardest part of programming is understanding the problem domain.

The problem domain represents all of the *bits* of information that make up the problem and restrict the scope of the solution.

A lot of his courses on pluralsight build the same application, but introduce new technologoies. The reason he does this is because it shifts the focus away from the problem domain and towards the technology he's trying to teach. Doing so makes life easier for both the teacher and student.

Writing code is a lot like a jigsaw puzzle - an inability to conceptualize the bigger picture and identify the main components makes the task at hand incredibly more difficult. With programming, this is usually the case. The problem domain is difficult to understand. To make programming easier, you can either make the problem domain easier or get better at understanding the problem domain. Don't make the mistake of jumping into a project without the requisite skills, information or analysis to succeed. You can easily end up wasting hours or even days trying to fix something you broke, when you could have spent that time gathering information and learning how to do it the right way.

*Make the problem domain easier on yourself through practice, preparation and acquiring neccessary information.*

## Object Literals

* Objects respresent real world things and have properties and methods
* Properties and methods are represented using variables and functions

### Object Literal Notation

    > let hotel = {
    >
    >    name: 'Quay'
    >    rooms: 40,
    >    booked: 25,
    >
    >   checkAvailability: function() {
        }    return this.rooms - this.booked;
    > };

### Accessing an Object and Dot Notation

    > let hotelName = hotel.name;
    > let roomsFree = hotel.checkAvailability();
    > let hotelName = hotel['name'];
    > let roomsFree = hotel['checkAvailability']();

    *square bracket syntax may be used in certain situations such as when the name has special characters*

## Document Object Model

* The DOM is how JavaScript accesses contents of a web page
* The DOM tree is a model of a web page and each DOM node is an object
* Use DOM Manipulation for secure data
* Four types of DOM nodes:
    1. document nodes
    1. element nodes
    1. attribute nodes
    1. text nodes

### Working with the DOM TREE

Access elements using DOM queries or by traversing the DOM

#### Accessing Elements

##### Selecting Individual Elements

> getElementById()
> querySelector() *uses a CSS selector*

##### Selecting Multiple Elements 

> getElementsByClassName()
> getElementsByTagName()
> querySelectorAll() - *uses CSS selector to select all matching elements*

##### Traversing Between Nodes

> parentNode
> previousSibling
> nextSibling
> firstChild
> lastChild

#### Working with Elements

##### Accessing Text Nodes

The nodeValue property lets you access or update contents of a node

* You can access and update text with textContent and innerText

##### Working with HTML Content

> innerHTML
> textContent
> createElement()
> createTextNode()
> appendChild()
> removeChild()

##### Accessing Attribute Values

hasAttribute()
getAttribute()
setAttribute()
removeAttribute()
