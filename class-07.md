[Table of Contents](https://peterjast.github.io/reading-notes/)

# **Object-Oriented Programming, HTML Tables**

## Domain Modeling

* A conceptual model to verify understanding of a specific problem

* An *object-oriented model* stores data in properties and encapsulates behavior in methods

* Use constructor functions to define the same properties between many objects

* tips for building domain models

> * Build self-contained objects with same attributes and behaviors to model many instances of the same thing
>
> * Use a constructor function that defines and intializes properties
>
> * Small and concise methods should be used to model behavior
>
> * Use the new keyword to create new instances
>
> * Store new instances in a new variable
>
> * use **this** keyword to access properties from within the object

## Tables

* Use tables to represent information in grid format

### Basic Table Structure

* table element is used to create a table

* tr element indicates start of new row

* td element respresents each cell

* th element is used for headings

* use rowspan or colspan to change the span of a cell

* thead, tbody, tfoot for long tables

> \<table>
>   \<tr>
>       \<td></td>
>       \<td></td>
>   \</tr>
>   \<tr>
>       \<td></td>
>       \<td></td>
>   \</tr>
>   \<tr>
>       \<td></td>
>       \<td></td>
>   \</tr>
> \<table>

## Functions, Methods, and Objects

* Use the new keyword and an object sontructor to create an object and then add properties and methods

### Constructor Notation - Creating an Object

    > let hotel = new Object();
    >
    >    hotel.name = 'Quay';
    >    hotel.rooms = 40;
    >    hotel.booked = 25;
    >
    >   hotel.checkAvailability = function() {
    >       return this.rooms - this.booked;    
    >    }    

### Update an Object

    >    hotel.name = 'Park';
    >    hotel['name'] = 'Park';

### Create Many Objects Using a Constructor Function

    > function Hotel(name, rooms, booked){}
    >
    >    this.hotel = name;
    >    this.rooms = rooms;
    >    this.booked = booked;
    >
    >   this.checkAvailability = function() {
    >       return this.rooms - this.booked;    
    >    }  
    > };
    >
    >   var quayHotel = new Hotel('Quay', 40, 25);
    >   var parkHotel = new Hotel('Park', 120, 77);

### Built-in Objects

* An object model represents real world things using a related group of objects

1. Browser Object Model - represent current window or tab
1. Document Object Model(DOM) - uses objects to represent current page
1. Global JavaScript Objects - things JS creates a model of(string, number, boolean, date, math, regex)