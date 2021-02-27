# Structure

How Pages Use Structure ?
Think about the stories you read in a newspaper: for each story, there will be a headline,
some text, and possibly some images. If the article is a long piece, there may be subheadings
that split the story into separate sections or quotes from those involved. Structure helps readers
understand the stories in the newspaper.
The structure is very similar when a news story is viewed online (although it may also
feature audio or video). This is illustrated on the right with a copy of a newspaper alongside
the corresponding article on its website.
Now think about a very different type of document — an insurance form. Insurance forms
often have headings for different sections, and each section contains a list of questions with
areas for you to fill in details or checkboxes to tick. Again, the structure is very similar online.

HTML Uses Elements to Describe the Structure of Pages:
Let's look closer at the code from the last page.There are several different elements. Each
element has an opening tag and a closing tag.

`<html>`

`<body>`

`<h1>This is the Main Heading</h1>`

`<p>This text might be an introduction to the rest of`
`the page. And if the page is a long one it might`
`be split up into several sub-headings.<p>`

`<h2>This is a Sub-Heading</h2>`

`<p>Many long articles have sub-headings so to help`
`you follow the structure of what is being written.`
`There may even be sub-sub-headings (or lower-level`
`headings).</p>`

`<h2>Another Sub-Heading</h2>`

`<p>Here you can see another sub-heading.</p>`

`</body>`

`</html>`

## Tags Body, Head & Title:

`<body>`

You met the "body` element in the first example we created.
Everything inside this element is shown inside the main browser window.


`<head>`

Before the body element you will often see a head element.
This contains information about the page (rather than information that is shown within
the main part of the browser window that is highlighted in blue on the opposite page).
You will usually find a <title> element inside the head element.
  
`<title>`

The contents of the <title> element are either shown in the top of the browser,
above where you usually type in the URL of the page you want to visit,or
on the tab for that page (if your browser uses tabs to allow you to view multiple pages at the same time).  

***

# Extra Markup

The Evolution of HTML:
Each new version was designed to be an improvement on the
last (with new elements and attributes added and older code removed).
HTML 4
Released 1997

XHTML 1.0
Released 2000

HTML5
Released 2000
"In HTML5, web page authors do not need to close all tags, and new elements and attributes will
be introduced. At the time of writing, the HTML5 specification had not been completed, but
the major browser makers had started to implement many of the new features, and web page
authors were rapidly adopting the new markup."

DOCTYPEs
HTML5
`<!DOCTYPE html>`

HTML 4
`<!DOCTYPE html PUBLIC`
`"-//W3C//DTD HTML 4.01 Transitional//EN"`
`"http://www.w3.org/TR/html4/loose.dtd">`

Transitional XHTML 1.0
`<!DOCTYPE html PUBLIC`
`"-//W3C//DTD XHTML 1.0 Transitional//EN"`
`"http://www.w3.org/TR/xhtml1/DTD/`
`xhtml1-transitional.dtd">`

Comments in HTML :
`<!-- -->`

ID Attribute :
`<p id="">`
  
Class Attribute :
 `<p class="">`

Block Elements :Some elements will always
appear to start on a new line in
the browser window. These are
known as block level elements.

Inline Elements :
`<em>  </b>`

Grouping Text & Elements In a Block :
`<div>`
  
Grouping Text &Elements Inline :
`<span>`
  
IFrames :
`<iframe>`
  
Information About Your Pages :
`<meta>`


***


## HTML5 Layout

### Traditional HTML Layouts:
For a long time, web page authors used <div> elements to group
together related elements on the page (such as the elements that form a
header, an article, footer or sidebar). Authors used class or id attributes
to indicate the role of the <div> element in the structure of the page.

![](https://i.postimg.cc/vHkQ6wHy/Untitsled.jpg)


### New Html 5 Layout Elements :

HTML5 introduces a new set of elements that allow you to divide up the
parts of a page. The names of these elements indicate the kind of content
you will find in them. They are still subject to change, but that has not
stopped many web page authors using them already.

![](https://i.postimg.cc/W4KmB3sK/Untitfsled.jpg)


### Headers & Footers
The `<header>` and `<footer>` elements can be used for:

● The main header or footer that appears at the top or bottom of every page on the site.

● A header or footer for an individual `<article>` or `<section>` within the page.

![](https://i.postimg.cc/qvM6LCPr/Untitfsled.jpg)
  

### Navigation `<nav>`

The <nav> element is used to contain the major navigational
blocks on the site such as the primary site navigation.

![](https://i.postimg.cc/XYJXF657/Untitfsled.jpg)

### Articles `<article>`

The <article> element acts as a container for any section of a
page that could stand alone and potentially be syndicated.

### Aside `<aside>`

The `<aside>` element has two purposes, depending on whether
it is inside an `<article>` element or not.

### Sections `<section>`

The <section> element groups related content together, and
typically each section would have its own heading.

### Heading Groups `<hgroup>`

The purpose of the `<hgroup>` element is to group together a
set of one or more `<h1>` through `<h6>` elements so that they are
treated as one single heading.

### Figures `<figure>` `<figcaption>`

You already met the `<figure>` element in Chapter 5 when we
looked at images. It can be used to contain any content that is
referenced from the main flow of an article (not just images).

### Sectioning Elements `<div>`

The <div> element will remain an important way to
group together related elements, because you should not be using
these new elements that you have just met for purposes other than those explicitly stated.

### Example HTML5 LAYOUT

![](https://i.postimg.cc/m23690sq/Untitfsled.jpg)

***

## Fundamentals to build a website such as :

1.Who is the Site For?

2.Why People Visit YOUR Website ?

3.What Your Visitors are Trying to Achieve ?

4.What Information Your Visitors Need ?

5.How Of ten People Will Visit Your Site ?

What is CSS?
CSS stands for Cascading Style Sheets CSS describes how HTML elements are to be displayed on screen, paper, or in other media CSS saves a lot of work. It can control the layout of multiple web pages all at once External stylesheets are stored in CSS files

Why Use CSS?
CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

CSS treats each HTML e XX lement as if it appears inside its own box and uses rules to indicate how that element should look.
Rules are made up of selectors (that specify the elements the rule applies to) and declarations (that indicate what these elements should look like).
Different types of selectors allow you to target your rules at different elements.
Declarations are made up of two parts: the properties of the element that you want to change, and the values of those properties. For example, the font-family property sets the choice of font, and the value arial specifies Arial as the preferred typeface.
CSS rules usually appear in a separate document, although they may appear within an HTML page.
Color
The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways: rgb values : These express colors in terms of how much red, green and blue are used to make it up. For example: rgb(100,100,90)

hex codes: These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. For example: #ee3e80 color names: There are 147 predefined color names that are recognized by browsers.
For example: DarkCyan We look at these three different ways of specifying colors on the next double-page spread.
CSS3 has also introduced another way to specify colors called HSLA.

***

## ABC of programming 

### What is a script and do i create one ?

A script is a series of instructions that a computer can follow to achieve a goal.

### WRITING A SCRIPT
To write a script, you need to first state your goal and then list the
tasks that need to be completed in order to achieve it.
Start with the big picture of what you want to achieve, and break
that down into smaller steps.

1: DEFINE THE GOAL
2: DESIGN THE SCRIPT
3: CODE EACH STEP

### How do computer fit in with the world around them ?

COMPUTERS CREATE MODELS OF THE WORLD USING DATA

### OBJECTS & PROPERTIES

OBJECTS (THINGS)
In computer programming, each physica l thing in the world can be represented as an object. There are
two different types of objects here: a hotel and a car.

PROPERTIES (CHARACTERISTICS)
Both of the cars share common characteristics. In fact, all cars have a make, a color, and engine
size. You could even determine their current speed. Programmers call these characteristics the
properties of an object.

### EVENTS

WHAT IS AN EVENT?
There are common ways in which people interact
with each type of object. For example, in a car a
driver will typically use at least two pedals. The car
has been designed to respond differently when the
driver interacts with each of the different pedals:
• The accelerator makes the car go faster
• The brake slows it down
Similarly, programs are designed to do different
things when users interact with the computer in
different ways. For example, clicking on a contact
link on a web page could bring up a contact
form, and entering text into a search box may
automatically trigger the search functionality.
An event is the computer's way of sticking up its
hand to say, "Hey, this just happened!"

WHAT DOES AN EVENT DO?
Programmers choose which events they respond to.
When a specific event happens, that event can be
used to trigger a specific section of the code.
Scripts often use different events to trigger different
types of functionality.
So a script will state which events the programmer
wants to respond to, and what part of the script
should be run when each of those events occur.

### METHODS

Methods represent things people need to do with objects. They can
retrieve or update the values of an object's properties.

WHAT IS A METHOD?
Methods typically represent how people (or otherthings) interact with an object in the real world.
They are like questions and instructions that:
• Tell you something about that object (using
information stored in its properties)
• Change the value of one or more of that object's
properties

WHAT DOES A METHOD DO?
The code for a method can contain lots of instructions that together represent one task.
When you use a method, you do not always need to know how it achieves its task; you just need to know
how to ask the question and how to interpret any answers it gives you.

PUTTING IT ALL TOGETHER

Computers use data to create models of things in the real world.
The events, methods, and properties of an object all relate to each other:
Events can trigger methods, and methods can retrieve or update an
object's properties.

### WEB BROWSERS ARE PROGRAMS BUILT USING OBJECTS

WINDOW OBJECT
On the right-hand page you can see a model of a computer with a browser open on the screen.
The browser represents each window or tab using a window object. The location property of the window
object will tell you the URL of the current page

DOCUMENT OBJECT
The current web page loaded into each window is modelled using a document object.
The title property of the document object tells you what is between the opening `<t; t le>` and closing
`</title>` tag for that web page, and the lastModified property of the document object
tells you the date this page was last updated.

### THE DOCUMENT OBJECT REPRESENTS AN HTML PAGE

Using the document object, you can access and change what content
users see on the page and respond to how they interact with it.

Like other objects that represent real-world things, the document object has:

PROPERTIES
Properties describe characteristics of the current web page (such as the t itle of the page).

METHODS
Methods perform tasks associated with the document currently loaded in the browser (such
as getting information from a specified element or adding new content).

EVENTS
You can respond to events, such as a user clicking or tapping on an element.

### HOW A BROWSER SEES A WEB PAGE

In order to understand how you can change the content of an HTML
page using JavaScript, you need to know how a browser interprets the HTML code and applies styling to it.

1: RECEIVE A PAGE AS HTML CODE Each page on a website can be seen as a separate document .
So, the web consists of many sites, each made up of one or more documents.

2: CREATE A MODEL OF THE PAGE AND STORE IT IN MEMORY The model shown on the right hand page is a representation
of one very basic page. Its structure is reminiscent of a family tree. At the top of the model is a document object,
which represents the whole document. Beneath the document object each box is called a node. Each of these nodes is
another object. This example features three types of nodes representing elements, text within the elements, and attribute.

3: USE A RENDERING ENGINE TO SHOW THE PAGE ON SCREEN If there is no CSS, the rendering engine will apply default styles
to HTML elements. However, the HTML code for this example links to a CSS style sheet, so the browser requests that file and
displays the page accordingly. When the browser receives CSS rules, the rendering engine processes them and applies
each rule to its corresponding elements. This is how the browser positions the elements in the correct place, with the
right colors, fonts, and so on.

### HOW DO I WRITE A SCRIPT FOR AWEB PAGE ?

HOW HTML, CSS, & JAVASCRIPT FIT TOGETHER

HTML ONLY
Starting with the HTML layer allows you to focus on the most important thing about your site:
its content. Being plain HTML, this layer should work on all kinds of
devices, be accessible to all users, and load quite quickly on
slow connections.

HTML+CSS
Adding the CSS rules in a separate file keeps rules regarding how the page looks
away from the content itself. You can use the same style sheet
with all of your site, making your sites faster to load and easier to maintain.
 Or you can use different style sheets with the same content to create different views of the same data.

HTML+CSS+JAVASCRIPT
The JavaScript is added last and enhances the usability of the page or the experience of
interacting with the site.
Keeping it separate means that the page still works if the user cannot load or run the
JavaScript. You can also reuse the code on several pages (making the site faster to load and easier to maintain).

