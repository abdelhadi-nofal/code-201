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

