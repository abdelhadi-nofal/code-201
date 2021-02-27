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


