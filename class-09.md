[Table of Contents](https://peterjast.github.io/reading-notes/)

# **Forms and JS Events**

## Forms

* use forms to collect information from users

* forms live in the form element

* form information is sent in name/value pairs

* each form control is given a name and user input is sent to the server
    
    > \<form action="http://www.example.com/review.php" method="get">
    > \<fieldset>
    > \<legend>
    >  Your Details:
    > \</legend>
    > \<label>
    > \<input type="text" name="username" size="15" maxlength="30" />
    > \</label>
    > \<br />
    > \<label>
    > \<textarea name="comments" cols="20" rows="4">Enter your comments...</textarea>
    > \</label>
    > \<br />
    > \<input type="radio" name="genre" value="rock" checked="checked" /> Rock
    > \<label>  
    > \<input type="checkbox" name="service" value="itunes" checked="checked" /> iTunes
    > \</label>
    > \<br>
    > \<label type="submit" value="Submit review" /> 
    > \</fieldset>
    > \</form>  

## Lists, Tables & Forms

* There are several CSS properties specifically used for lists, tables and forms

* Use the list-style-type and list-style image properties to give list markers different appearances

* Several properties allow you to control table cell borders and spacing

* aligning form controls vertically using CSS makes forms much easier to use

* Styling makes forms feel more interactive

## Events

* Events are how the browser knows when something happens

* Binding states which event and element you are waiting for

* Events can trigger JavaScript functions

* Events and JS functions make the page feel interactice

* You can monitor events on all children of an element

* W3C DOM events are most common, but there are other events such as browser events