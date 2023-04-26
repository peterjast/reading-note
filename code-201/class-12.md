# **Chart.js, Canvas**

## Chart.js

* Use to create stunning animated charts

* Charts are better than tables for displaying data

* Charts.js is a JS plugin that uses the canvas element to draw a graph

* You can use it to make bar charts, line charts, pie charts, etc.

### Setting Up

1. download chart.js here [https://github.com/chartjs/Chart.js](https://github.com/chartjs/Chart.js)

1. copy Chart.min.js out of the unzipped folder into your project directory

1. import the script in your html
    > \<script src='Chart.min.js'></script>

### Drawing a line chart

1. Create a canvas element in body of our HTML
    > \<canvas id="buyers" width="600" height="400"></canvas>

1. write a script that will retrieve context of canvas and add to foot of body element
    > \<script>
    >
    > var buyers = document.getElementById('buyers').getContext('2d');
    >
    > new Chart(buyers).Line(buyerData);
    >
    > \</script>

1. inside script tag, pass options to chart using Line method or create data
    > var buyerData = {
    >
    > labels : ["January","February","March","April","May","June"],
    >
    > datasets : [
    >
    > {
    >
    > fillColor : "rgba(172,194,132,0.4)",
    >
    > strokeColor : "#ACC26D",
    >
    > pointColor : "#fff",
    >
    > pointStrokeColor : "#9DB86D",
    >
    > data : [203,156,99,251,305,247]
    >
    > }
    >
    > ]
    >
    > }

*All code examples are from the following article. Please refer to this article for more information* 

[https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

### Resources

Documentation: [https://www.chartjs.org/docs/latest/](https://www.chartjs.org/docs/latest/)

Github: [https://github.com/chartjs/Chart.js](https://github.com/chartjs/Chart.js)

## Canvas

* Canvas element looks like image element

* Only two attributes, width and height

* Can be styles like any normal image

* easily define fallback context

* requires closing tag

* rendering context using getContext method takes on parameter, type of context

View these resources for examples:

[Basic Usage](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

[Drawing shapes](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

[Applying styles and Colors](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

[Drawing Text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)

[<=== Back to Table of Contents](https://peterjstaker.github.io/reading-notes/)
