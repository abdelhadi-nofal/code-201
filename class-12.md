## Chart.js API

Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.

A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.

To see how to use chart.js we’re going to create a set of 3 graphs; one will show the number of buyers a fictional product has over the course of 6 months, this will be a line chart; the second will show which countries the customers come from, this will be the pie chart; finally we’ll use a bar chart to show profit over the period.

 

Setting up
The first thing we need to do is download Chart.js. Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in. Then create a new html page and import the script:

`<!DOCTYPE html>`
`<html lang="en">`
    `<head>`
        `<meta charset="utf-8" />`
        `<title>Chart.js demo</title>`
        `<script src='Chart.min.js'></script>`
    `</head>`
    `<body>`
    `</body>`
`</html>`

Drawing a line chart
To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart. So add this to the body of our HTML page:

`<canvas id="buyers" width="600" height="400"></canvas>`


Next, we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element:

`<script>`
    `var buyers = document.getElementById('buyers').getContext('2d');`
    `new Chart(buyers).Line(buyerData);`
`</script>`


(We can actually pass some options to the chart via the Line method, but we’re going to stick to the data for now to keep it simple.)

Inside the same script tags we need to create our data, in this instance it’s an object that contains labels for the base of our chart and datasets to describe the values on the chart. Add this immediately above the line that begins ‘var buyers=’:

`var buyerData = {`
	`labels : ["January","February","March","April","May","June"],`
	`datasets : [`
		`{`
			`fillColor : "rgba(172,194,132,0.4)",`
			`strokeColor : "#ACC26D",`
			`pointColor : "#fff",`
			`pointStrokeColor : "#9DB86D",`
			`data : [203,156,99,251,305,247]`
		`}`
	`]`
`}`


If you test your file in a browser you’ll now see a cool animated line graph.

 

Drawing a pie chart
Our line chart is complete, so let’s move on to our pie chart. First, we need the canvas element:

<canvas id="countries" width="600" height="400"></canvas>
Next, we need to get the context and to instantiate the chart:

var countries= document.getElementById("countries").getContext("2d");
new Chart(countries).Pie(pieData, pieOptions);
You’ll notice that this time, we are going to supply some options to the chart.

Next we need to create the data. This data is a little different to the line chart because the pie chart is simpler, we just need to supply a value and a color for each section:

`var pieData = [`
	`{`
		`value: 20,`
		`color:"#878BB6"`
	`},`
	`{`
		`value : 40,`
		`color : "#4ACAB4"`
	`},`
	`{`
		`value : 10,`
		`color : "#FF8153"`
	`},`
	`{`
		`value : 30,`
		`color : "#FFEA88"`
	`}`
`];`

`Now, immediately after the pieData we’ll add our options:`

`var pieOptions = {`
	`segmentShowStroke : false,`
	`animateScale : true`
`}`


These options do two things, first they remove the stroke from the segments, and then they animate the scale of the pie so that it zooms out from nothing.

 

Drawing a bar chart
Finally, let’s add  a bar chart to our page. Happily the syntax for the bar chart is very similar to the line chart we’ve already added. First, we add the canvas element:

<canvas id="income" width="600" height="400"></canvas>
Next, we retrieve the element and create the graph:

var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);
And finally, we add in the bar chart’s data:

``var barData = {``
	``labels : ["January","February","March","April","May","June"],``
	``datasets : [``
		``{``
			``fillColor : "#48A497",``
			``strokeColor : "#48A4D1",``
			``data : [456,479,324,569,702,600]``
		``},``
		``{``
			``fillColor : "rgba(73,188,170,0.4)",``
			``strokeColor : "rgba(72,174,209,0.4)",``
			``data : [364,504,605,400,345,320]``
		``}``

	``]``
``}``


As you can see, the data is largely the same, except this time we’ve chosen to use RGBA to specify our colors which allows us to add transparency.

 

Conclusion
You can view a demo of this in action here, and if you prefer copy and paste, here is the full script:

`<!DOCTYPE html>`
`<html lang="en">`
    `<head>`
        `<meta charset="utf-8" />`
        `<title>Chart.js demo</title>`
        `<!-- import plugin script -->`
        `<script src='Chart.min.js'></script>`
    `</head>`
    `<body>`
        `<!-- line chart canvas element -->`
        `<canvas id="buyers" width="600" height="400"></canvas>`
        `<!-- pie chart canvas element -->`
        `<canvas id="countries" width="600" height="400"></canvas>`
        `<!-- bar chart canvas element -->`
        `<canvas id="income" width="600" height="400"></canvas>`
        `<script>`
            `// line chart data`
            `var buyerData = {`
                `labels : ["January","February","March","April","May","June"],`
                `datasets : [`
                `{`
                    `fillColor : "rgba(172,194,132,0.4)",`
                    `strokeColor : "#ACC26D",`
                    `pointColor : "#fff",`
                    `pointStrokeColor : "#9DB86D",`
                    `data : [203,156,99,251,305,247]`
                `}`
            `]`
            `}`
            `// get line chart canvas`
            `var buyers = document.getElementById('buyers').getContext('2d');`
            `// draw line chart`
            `new Chart(buyers).Line(buyerData);`
            `// pie chart data`
            `var pieData = [`
                `{`
                    `value: 20,`
                    `color:"#878BB6"`
                `},`
                `{`
                    `value : 40,`
                    `color : "#4ACAB4"`
                `},`
                `{`
                    `value : 10,`
                    `color : "#FF8153"`
                `},`
                `{`
                    `value : 30,`
                    `color : "#FFEA88"`
                `}`
            `];`
            `// pie chart options`
            `var pieOptions = {`
                 `segmentShowStroke : false,`
                 `animateScale : true`
            `}`
            `// get pie chart canvas`
            `var countries= document.getElementById("countries").getContext("2d");`
            `// draw pie chart`
            `new Chart(countries).Pie(pieData, pieOptions);`
            `// bar chart data`
            `var barData = {`
                `labels : ["January","February","March","April","May","June"],`
                `datasets : [`
                    `{`
                        `fillColor : "#48A497",`
                        `strokeColor : "#48A4D1",`
                        `data : [456,479,324,569,702,600]`
                    `},`
                    `{`
                        `fillColor : "rgba(73,188,170,0.4)",`
                        `strokeColor : "rgba(72,174,209,0.4)",`
                        `data : [364,504,605,400,345,320]`
                    `}`
                `]`
            `}`
            `// get bar chart canvas`
            `var income = document.getElementById("income").getContext("2d");`
            `// draw bar chart`
            `new Chart(income).Bar(barData);`
        `</script>`
    `</body>`
`</html>`


Installation

You can download the latest version of Chart.js from the GitHub releases or use a Chart.js CDN. Detailed installation instructions can be found on the installation page.

Creating a Chart
It's easy to get started with Chart.js. All that's required is the script included in your page along with a single <canvas> node to render the chart.

In this example, we create a bar chart for a single dataset and render that in our page. You can see all the ways to use Chart.js in the usage documentation.


`<canvas id="myChart" width="400" height="400"></canvas>`
`<script>`
`var ctx = document.getElementById('myChart').getContext('2d');`
`var myChart = new Chart(ctx, {`
    `type: 'bar',`
    `data: {`
        `labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],`
        `datasets: [{`
            `label: '# of Votes',`
            `data: [12, 19, 3, 5, 2, 3],`
            `backgroundColor: [`
                `'rgba(255, 99, 132, 0.2)',`
                `'rgba(54, 162, 235, 0.2)',`
                `'rgba(255, 206, 86, 0.2)',`
                `'rgba(75, 192, 192, 0.2)',`
                `'rgba(153, 102, 255, 0.2)',`
                `'rgba(255, 159, 64, 0.2)'`
            `],`
            `borderColor: [`
                `'rgba(255, 99, 132, 1)',`
                `'rgba(54, 162, 235, 1)',`
                `'rgba(255, 206, 86, 1)',`
                `'rgba(75, 192, 192, 1)',`
                `'rgba(153, 102, 255, 1)',`
                `'rgba(255, 159, 64, 1)'`
            `],`
            `borderWidth: 1`
        `}]`
    `},`
    `options: {`
        `scales: {`
            `yAxes: [{`
                `ticks: {`
                    `beginAtZero: true`
                `}`
            `}]`
        `}`
    `}`
`});`
`</script>`


Contributing

Before submitting an issue or a pull request to the project, please take a moment to look over the contributing guidelines first.

For support using Chart.js, please post questions with the chartjs tag on Stack Overflow.

License

Chart.js is available under the MIT license.

## Basic usage of canvas

Let's start this tutorial by looking at the <canvas> HTML element itself. At the end of this page, you will know how to set up a canvas 2D context and have drawn a first example in your browser.

The <canvas> element
<canvas id="tutorial" width="150" height="150"></canvas>
At first sight a <canvas> looks like the <img> element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the <canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

Note: If your renderings seem distorted, try specifying your width and height attributes explicitly in the <canvas> attributes, and not using CSS.

The id attribute isn't specific to the <canvas> element but is one of the global HTML attributes which can be applied to any HTML element (like class for instance). It is always a good idea to supply an id because this makes it much easier to identify it in a script.

The <canvas> element can be styled just like any normal image (margin, border, background…). These rules, however, don't affect the actual drawing on the canvas. We'll see how this is done in a dedicated chapter of this tutorial. When no styling rules are applied to the canvas it will initially be fully transparent.

Fallback content
The <canvas> element differs from an <img> tag in that, like for <video>, <audio>, or <picture> elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers.

Providing fallback content is very straightforward: just insert the alternate content inside the <canvas> element. Browsers that don't support <canvas> will ignore the container and render the fallback content inside it. Browsers that do support <canvas> will ignore the content inside the container, and just render the canvas normally.

For example, we could provide a text description of the canvas content or provide a static image of the dynamically rendered content. This can look something like this:

`<canvas id="stockGraph" width="150" height="150">`
  `current stock price: .15 + 0.15`
`</canvas>`

`<canvas id="clock" width="150" height="150">`
  `<img src="images/clock.png" width="150" height="150" alt=""/>`
`</canvas>`


Telling the user to use a different browser that supports canvas does not help users who can't read the canvas at all, for example. Providing a useful fallback text or sub DOM helps to make the canvas more accessible.

Required </canvas> tag
As a consequence of the way fallback is provided, unlike the <img> element, the <canvas> element requires the closing tag (</canvas>). If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.

If fallback content is not needed, a simple <canvas id="foo" ...></canvas> is fully compatible with all browsers that support canvas at all.

The rendering context
The <canvas> element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, WebGL uses a 3D context based on OpenGL ES.

The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. The <canvas> element has a method called getContext(), used to obtain the rendering context and its drawing functions. getContext() takes one parameter, the type of context. For 2D graphics, such as those covered by this tutorial, you specify "2d" to get a CanvasRenderingContext2D.

var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
The first line in the script retrieves the node in the DOM representing the <canvas> element by calling the document.getElementById() method. Once you have the element node, you can access the drawing context using its getContext() method.

Checking for support
The fallback content is displayed in browsers which do not support <canvas>. Scripts can also check for support programmatically by testing for the presence of the getContext() method. Our code snippet from above becomes something like this:

`var canvas = document.getElementById('tutorial');`

`if (canvas.getContext) {`
  `var ctx = canvas.getContext('2d');`
  `// drawing code here`
`} else {`
  `// canvas-unsupported code here`
`}`


A skeleton template
Here is a minimalistic template, which we'll be using as a starting point for later examples.

Note: it is not good practice to embed a script inside HTML. We do it here to keep the example concise.

`<!DOCTYPE html>`
`<html>`
  `<head>`
    `<meta charset="utf-8"/>`
    `<title>Canvas tutorial</title>`
    `<script type="text/javascript">`
      `function draw() {`
        `var canvas = document.getElementById('tutorial');`
        `if (canvas.getContext) {`
          `var ctx = canvas.getContext('2d');`
        `}`
      `}`
    `</script>`
    `<style type="text/css">`
      `canvas { border: 1px solid black; }`
    `</style>`
  `</head>`
  `<body onload="draw();">`
    `<canvas id="tutorial" width="150" height="150"></canvas>`
  `</body>`
`</html>`


The script includes a function called draw(), which is executed once the page finishes loading; this is done by listening for the load event on the document. This function, or one like it, could also be called using window.setTimeout(), window.setInterval(), or any other event handler, as long as the page has been loaded first.

A simple example

To begin, let's take a look at a simple example that draws two intersecting rectangles, one of which has alpha transparency. We'll explore how this works in more detail in later examples.

`<!DOCTYPE html>`
`<html>`
 `<head>`
  `<meta charset="utf-8"/>`
  `<script type="application/javascript">`
    `function draw() {`
      `var canvas = document.getElementById('canvas');`
      `if (canvas.getContext) {`
        `var ctx = canvas.getContext('2d');`

        `ctx.fillStyle = 'rgb(200, 0, 0)';`
        `ctx.fillRect(10, 10, 50, 50);`

        `ctx.fillStyle = 'rgba(0, 0, 200, 0.5)';`
        `ctx.fillRect(30, 30, 50, 50);`
      `}`
    `}`
  `</script>`
 `</head>`
 `<body onload="draw();">`
   `<canvas id="canvas" width="150" height="150"></canvas>`
 `</body>`
`</html>`


## Drawing shapes with canvas

Now that we have set up our canvas environment, we can get into the details of how to draw on the canvas. By the end of this article, you will have learned how to draw rectangles, triangles, lines, arcs and curves, providing familiarity with some of the basic shapes. Working with paths is essential when drawing objects onto the canvas and we will see how that can be done.

The grid
Before we can start drawing, we need to talk about the canvas grid or coordinate space. Our HTML skeleton from the previous page had a canvas element 150 pixels wide and 150 pixels high. To the right, you see this canvas with the default grid overlayed. Normally 1 unit in the grid corresponds to 1 pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0,0). All elements are placed relative to this origin. So the position of the top left corner of the blue square becomes x pixels from the left and y pixels from the top, at coordinate (x,y). Later in this tutorial we'll see how we can translate the origin to a different position, rotate the grid and even scale it, but for now we'll stick to the default.

Drawing rectangles
Unlike SVG, <canvas> only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths. Luckily, we have an assortment of path drawing functions which make it possible to compose very complex shapes.

First let's look at the rectangle. There are three functions that draw rectangles on the canvas:

fillRect(x, y, width, height)
Draws a filled rectangle.
strokeRect(x, y, width, height)
Draws a rectangular outline.
clearRect(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.
Each of these three functions takes the same parameters. x and y specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. width and height provide the rectangle's size.

Below is the draw() function from the previous page, but now it is making use of these three functions.

Rectangular shape example


``function draw() {``
  ``var canvas = document.getElementById('canvas');``
  ``if (canvas.getContext) {``
    ``var ctx = canvas.getContext('2d');``

    ``ctx.fillRect(25, 25, 100, 100);``
    ``ctx.clearRect(45, 45, 60, 60);``
    ``ctx.strokeRect(50, 50, 50, 50);``
  ``}``
``}``


Drawing paths
Now let's look at paths. A path is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed. To make shapes using paths, we take some extra steps:

First, you create the path.
Then you use drawing commands to draw into the path.
Once the path has been created, you can stroke or fill the path to render it.
Here are the functions used to perform these steps:

beginPath()
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
Path methods
Methods to set different paths for objects.
closePath()
Adds a straight line to the path, going to the start of the current sub-path.
stroke()
Draws the shape by stroking its outline.
fill()
Draws a solid shape by filling the path's content area.
The first step to create a path is to call the beginPath(). Internally, paths are stored as a list of sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is reset and we can start drawing new shapes.

### Applying styles and colors

In the chapter about drawing shapes, we used only the default line and fill styles. Here we will explore the canvas options we have at our disposal to make our drawings a little more attractive. You will learn how to add different colors, line styles, gradients, patterns and shadows to your drawings.

Colors
Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

fillStyle = color
Sets the style used when filling shapes.
strokeStyle = color
Sets the style for shapes' outlines.
color is a string representing a CSS <color>, a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value #000000).

Note: When you set the strokeStyle and/or fillStyle property, the new value becomes the default for all shapes being drawn from then on. For every shape you want in a different color, you will need to reassign the fillStyle or strokeStyle property.

The valid strings you can enter should, according to the specification, be CSS <color> values. Each of the following examples describe the same color.

// these all set the fillStyle to 'orange'

ctx.fillStyle = 'orange';
ctx.fillStyle = '#FFA500';
ctx.fillStyle = 'rgb(255, 165, 0)';
ctx.fillStyle = 'rgba(255, 165, 0, 1)';
A fillStyle example
In this example, we once again use two for loops to draw a grid of rectangles, each in a different color. The resulting image should look something like the screenshot. There is nothing too spectacular happening here. We use the two variables i and j to generate a unique RGB color for each square, and only modify the red and green values. The blue channel has a fixed value. By modifying the channels, you can generate all kinds of palettes. By increasing the steps, you can achieve something that looks like the color palettes Photoshop uses.

`function draw() {`
  `var ctx = document.getElementById('canvas').getContext('2d');`
  `for (var i = 0; i < 6; i++) {`
    `for (var j = 0; j < 6; j++) {`
      `ctx.fillStyle = 'rgb(' + Math.floor(255 - 42.5 * i) + ', ' +`
                       `Math.floor(255 - 42.5 * j) + ', 0)';`
      `ctx.fillRect(j * 25, i * 25, 25, 25);`
    `}`
  `}`
`}`

### Drawing text

Drawing text
The canvas rendering context provides two methods to render text:

fillText(text, x, y [, maxWidth])
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
strokeText(text, x, y [, maxWidth])
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.
A fillText example
The text is filled using the current fillStyle.

`function draw() {`
  `var ctx = document.getElementById('canvas').getContext('2d');`
  `ctx.font = '48px serif';`
  `ctx.fillText('Hello world', 10, 50);`
`}`

Styling text
In the examples above we are already making use of the font property to make the text a bit larger than the default size. There are some more properties which let you adjust the way the text gets displayed on the canvas:

font = value
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
textAlign = value
Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
textBaseline = value
Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
direction = value
Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.
These properties might be familiar to you, if you have worked with CSS before.

The following diagram from the WHATWG demonstrates the various baselines supported by the textBaseline property.

Advanced text measurements
In the case you need to obtain more details about the text, the following method allows you to measure it.

measureText()
Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style.
The following code snippet shows how you can measure a text and get its width.

Gecko-specific notes
In Gecko (the rendering engine of Firefox, Firefox OS and other Mozilla based applications), some prefixed APIs were implemented in earlier versions to draw text on a canvas. These are now deprecated and removed, and are no longer guaranteed to work.










