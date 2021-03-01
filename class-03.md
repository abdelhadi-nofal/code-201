## Lists

There are lots of occasions when we
need to use lists. HTML provides us with
three different types:

● Ordered lists are lists where each item in the list is
numbered. For example, the list might be a set of steps for
a recipe that must be performed in order, or a legal contract
where each point needs to be identified by a section
number.
● Unordered lists are lists that begin with a bullet point
(rather than characters that indicate order).
● Definition lists are made up of a set of terms along with the
definitions for each of those terms.

Ordered Lists `<ol><li>`

Unordered Lists `<ul><li>`

Definition Lists  `<dl>  <dt>  <dd>`

Nested Lists  
You can put a second list insidean <li> element to create a sublistor nested list.
Browsers display nested lists indented further than the parent list. In nested unordered lists, the browser will usually change
the style of the bullet point too.

Example
`<html>`
`<head>`
`<title>Lists</title>`
`</head>`
`<body>`
`<h1>Scrambled Eggs</h1>`
`<p>Eggs are one of my favourite foods. Here is a`
`recipe for deliciously rich scrambled eggs.</p>`
`<h2>Ingredients</h2>`
`<ul>`
`<li>2 eggs</li>`
`<li>1tbs butter</li>`
`<li>2tbs cream</li>`
`</ul>`
`<h2>Method</h2>`
`<ol>`
`<li>Melt butter in a frying pan over a medium`
`heat</li>`
`<li>Gently mix the eggs and cream in a bowl</li>`
`<li>Once butter has melted add cream and eggs</li>`
`<li>Using a spatula fold the eggs from the edge of`
`the pan to the center every 20 seconds (as if`
`you are making an omelette)</li>`
`<li>When the eggs are still moist remove from the`
`heat (it will continue to cook on the plate`
`until served)</li>`
`</ol>`
`</body>`
`</html>`

***

## Boxes

At the beginning of this section on CSS, you saw how CSS treats each HTML
element as if it lives in its own box. You can set several properties that affect the appearance of
these boxes. In this chapter you will see how to: 
● Control the dimensions of your boxes
● Create borders around boxes
● Set margins and padding for boxes
● Show and hide boxes
Once you have learned how to control the appearance of each
box, you will see how to position these boxes on your pages in
Chapter 15 when we look at page layout.

BOX DIMENTION
width, height

By default a box is sized just big
enough to hold its contents. To
set your own dimensions for a
box you can use the height and
width properties.
The most popular ways to
specify the size of a box are
to use pixels, percentages, or
ems. Traditionally, pixels have
been the most popular method
because they allow designers to
accurately control their size.
When you use percentages,
the size of the box is relative to
the size of the browser window
or, if the box is encased within
another box, it is a percentage of
the size of the containing box.


Limiting Width
min-width, max-width

Some page designs expand and
shrink to fit the size of the user's
screen. In such designs, the
min-width property specifies
the smallest size a box can be
displayed at when the browser
window is narrow, and the
max-width property indicates
the maximum width a box can
stretch to when the browser
window is wide.


LIMITING HEIGHT
min-height, max-height

In the same way that you might
want to limit the width of a box
on a page, you may also want
to limit the height of it. This is
achieved using the min-height
and max-height properties.
The example on this page
demonstrates these properties
in action. It also shows you what
happens when the content of the
box takes up more space than
the size specified for the box.


Overflowing Content

The overflow property tells the
browser what to do if the content
contained within a box is larger
than the box itself. It can have
one of two values:

* hidden
* scroll


Border, Margin& Padding

Every box has three available properties that
can be adjusted to control its appearance:

Border, Margin & Padding
1.Border

Every box has a border (even if
it is not visible or is specified to
be 0 pixels wide). The border
separates the edge of one box
from another.
2. Margin
Margins sit outside the edge
of the border. You can set the
width of a margin to create a
gap between the borders of two
adjacent boxes.
3.Padding
Padding is the space between
the border of a box and any
content contained within it.
Adding padding can increase the
readability of its contents.

Centering Content

If you want to center a box on
the page (or center it inside
the element that it sits in), you
can set the left-margin and
right-margin to auto.
In order to center a box on the
page, you need to set a width
for the box (otherwise it will take
up the full width of the page).

Change Inline/Block

display
The display property allows
you to turn an inline element
into a block-level element or vice
versa, and can also be used to
hide an element from the page.
The values this property can
take are:

* inline
* block
* inline-block
* none


CSS3: Border Images

The border-image property
applies an image to the border of
any box. It takes a background
image and slices it into nine
pieces.
Here is the image. I have
added marks where it is
sliced in the example,
taking 18 pixels from each corner
to place an entire circle in each
corner. The corner slices are
always placed in the four corners
of the box, but we have a choice
whether the sides are stretched
or repeated.

Example

`<!DOCTYPE html>`
`<html>`
`<head>`
`<title>Boxes</title>`
`<style type="text/css">`
`body {`
`font-size: 80%;`
`font-family: "Courier New", Courier, monospace;`
`letter-spacing: 0.15em;`
`background-color: #efefef;}`
`#page {`
`max-width: 940px;`
`min-width: 720px;`
`margin: 10px auto 10px auto;`
`padding: 20px;`
`border: 4px double #000;`
`background-color: #ffffff;}`
`#logo {`
`width: 150px;`
`margin: 10px auto 25px auto;}`
`ul {`
`width: 570px;`
`padding: 15px;`
`margin: 0px auto 0px auto;`
`border-top: 2px solid #000;`
`border-bottom: 1px solid #000;`
`text-align: center;}`
`li {`
`display: inline;`
`margin: 0px 3px;}`
`p {`
`text-align: center;`
`width: 600px;`
`margin: 20px auto 20px auto;`
`font-weight: normal;}`

***

## Decisions and Loops

Decision Making Statements
Decision Making in programming is similar to decision making in real life.
A programming language uses control statements to control the flow of execution of the program based on certain conditions.
JavaScript’s conditional statements are:
1) if
2) if-else
3) if…else…if
4) switch
1) if statement
if statement is the most simple decision making statement.
It is used to decide whether a certain statement or block of statements will be executed or not.
If a certain condition is true then a block of statement is executed otherwise not.
Syntax
`if ( condition ) `
`{`
   `// block of code to be executed`
`}`

2) if…else statement
The if-else statement has two parts if block and else block.
If the condition is true then if block (true block) will get executed and if the condition is false then else block (false block) will get executed.
Syntax

`if ( condition )  `
`{`
    `// block of code to be executed when condition is true`
`} `
`else `
`{`
    `// block of code to be executed when condition is false`
`}`

3) if…else...if statement
The if…else…if statement statement is an advanced form of if…else that allows JavaScript to make a correct decision out of several conditions.
All the if conditions will be checked one by one. If any condition is true out of given then that block will get executed and other blocks are skipped.
Syntax

`if ( condition 1 )  `
`{`
    `// block of code to be executed when condition 1 is true`
`} `
`else if ( condition 2 )  `
`{`
    `// block of code to be executed when condition 2 is true`
`} `
`else if ( condition 3 )  `
`{`
    `// block of code to be executed when condition 2 is true`
`}`
`else`
`{`
   `// block of code to be executed if no condition matches`
`}`

4) switch statement
The objective of a switch statement is to give an expression to evaluate and several different statements to execute based on the value of the expression.
The interpreter checks each case against the value of the expression until a match is found. If nothing matches, a default condition will be used.
Syntax

`switch (expression) `
`{`
   `case c1: statement(s)`
            `break;`
   
   `case c2: statement(s)`
            `break;`
   `...`
   
   `case cn: statement(s)`
            `break;`
   
   `default: statement(s)`
`}`

Looping Statements
Looping in programming languages facilitates the execution of a set of instructions/functions repeatedly while some condition evaluates to true.
For example, suppose we want to print “Hello World” 10 times this is possible with the help of loops.
There are mainly two types of loops:
1) Entry Controlled loops: In this type of loops the test condition is tested before entering the loop body. For Loop and While Loop are entry controlled loops.
2) Exit Controlled Loops: In this type of loops the test condition is tested or evaluated at the end of loop body. Therefore, the loop body will execute atleast once, irrespective of whether the test condition is true or false. do-while loop is exit controlled loop.
Following are the types of loops in JavaScript:
1) while loop
2) do-while loop
3) for loop
4) for…in loop
1) while loop
A while loop is a entry-controlled loop that allows code to be executed repeatedly if the condition is true.
When the condition becomes false, the loop terminates which marks the end of its life cycle.
The while loop executes ZERO or MORE times.
Syntax

`while (condition)`
`{`
   `// Statements to be executed`
`}`

2) do-while loop
A do-while loop is a exit-controlled loop that allows code to be executed first and after that checks for condition and depending on that it executed repeatedly.
When the condition becomes false, the loop terminates which marks the end of its life cycle.
The do-while loop executes ONE or MORE times.
Syntax

`do`
`{`
    `// Statements to be executed`
`}  while (condition);`

3) for loop
A for loop is a entry-controlled loop that allows code to be executed repeatedly.
It provides a concise way of writing the loop structure.
Unlike a while loop, a for statement consumes the initialization, condition and increment/decrement in one line thereby providing a shorter, easy to debug structure of looping.
The for loop executes ZERO or MORE times
Syntax

`for (initialization; condition; increment/decrement)`
`{`
    `// Statements to be executed`
`}`

4) for…in loop
JavaScript also includes another version of for loop also known as the for..in loops.
The for..in loop provides a simpler way to iterate through the properties of an object.
This loop is seen to be very useful while working with objects.
In each iteration, one of the properties of Object is assigned to the variable named variableName and this loop continues until all of the properties of the Object are processed.
Syntax

`for (variableName in Object)`
`{`
    `// Statements to be executed`
`}`

### SAMPLE PROGRAMS
Develop a JS program to display numbers from 1 to 10.

`<html>`
    `<head>`
        `<title>Display Numbers from 1 to 10</title>`
    `</head>`
    `<body>`
        `<h3>Numbers from 1 to 10 are</h3>`
        `<script type="text/javascript">`
            `var a = 1; `
  
            `while (a <= 10) `
            `{ `
                `document.write(a + "<br />"); `
                `a++; `
            `}`
        `</script>`
    `</body>`
`</html>`

