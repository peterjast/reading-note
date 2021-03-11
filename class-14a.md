# **CSS Transforms, Transitions, and Animations**

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## Transforms

All code samples are from [https://learn.shayhowe.com/advanced-html-css/css-transforms/](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

* **transform** property settings
    1. two dimensional
    1. three dimensional

* browser support for transform isn't great, but improving

### Transform Syntax

* include transform property followed by value

* value is transform type and amount in parenthesis

> div {
>
> -webkit-transform: scale(1.5);
>
>     -moz-transform: scale(1.5);
>
>       -o-transform: scale(1.5);
>
>          transform: scale(1.5);
>
> }

### Tranform Origin

* By default, center of element

* can be changed using transform-origin property

* accepts one or two values for each axis

### 2D Transforms

* work on x and y axes

* rotate, scale, translate, skew, perspective

* you can combine transformations

### 3D Transforms

* x, y and z axes

* rotate, scale, translate, skew

* Transform style: transform-style property, preserve-3d value

* backface-visibility hidden or visible

Read this article for more information on CSS transforms [https://learn.shayhowe.com/advanced-html-css/css-transforms/](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

## Transitions & Animations

Code samples are from [https://learn.shayhowe.com/advanced-html-css/transitions-animations/](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

* Transitions alter appearance and behavior from one state to another

* Animations altear appearance and behavior in multiple keyframes

## Transitions

* element must have change in state

* :hover, :focus, :active, :target

* 4 total properties
    1. transition-property
    1. transition-duration
    1. transition-timing-function
    1. transition-delay

> .box {
>  
> background: #2db34a;
>
> transition-property: background;
>
> transition-duration: 1s;
>
> transition-timing-function: linear;
>
> }
>
> .box:hover {
>
> background: #ff7b29;
>
> }

* transition-property is what properties will be altered

* transition-duration is how long a transition takes place

* transition-timing-function sets speed the transition will move

* transition delay is how long a transition waits before executing

## Animations

Code samples are from [https://learn.shayhowe.com/advanced-html-css/transitions-animations/](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

* Animations give you more control than transitions which require multiple states

* Use @keyframes rul to set multiple points an element should transition

> @keyframes slide {
>
> 0% {
>
> left: 0;
>
> top: 0;
>
> }
>
> 50% {
>
> left: 244px;
>
> top: 100px;
>
> }
>
> 100% {
>
> left: 488px;
>
> top: 0;
>
> }
>
> }

For more information about transitions or animations read this article [https://learn.shayhowe.com/advanced-html-css/transitions-animations/](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

Additional Resources:

[8 simple CSS3 transitions that will wow your users](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

[6 Buttons animated](http://codepen.io/retyui/pen/ByoaXV)

[CSS3 Animations: Keyframes](http://codepen.io/akshaychauhan/pen/oAfae)

[404](http://codepen.io/kieranfivestars/pen/MYdQxX)

[Pure CSS Bounce Animation](http://codepen.io/dp_lewis/pen/gCfBv)
