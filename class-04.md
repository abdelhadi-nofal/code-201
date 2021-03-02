## Links 4

### Writing Links

Links are created using the <a> element. Users can click on anything
between the opening <a> tag and the closing `</a>` tag. You specify
which page you want to link to using the href attribute.
`<a href="http://www.imdb.com">IMDB</a>`

Linking to Other Sites `<a>`

Links are created using the `<a>` element which has an attribute
called href. The value of the href attribute is the page that
you want people to go to when they click on the link.
Users can click on anything that appears between the opening
`<a>` tag and the closing `</a>` tag and will be taken to the page
specified in the href attribute. When you link to a different
website, the value of the href attribute will be the full web
address for the site, which is known as an absolute URL.

### Directory Structure
On larger websites it's a good idea to organize your code by placing the
pages for each different section of the site into a new folder. Folders on a
website are sometimes referred to as directories.

* Structure
The diagram on the right shows
the directory structure for a
fictional entertainment listings
website called ExampleArts.

* Relationships
The relationship between
files and folders on a website
is described using the same
terminology as a family tree.

* Homepages
The main homepage of a site
written in HTML (and the
homepages of each section in a
child folder) is called index.html.

### Relative URLs

Relative URLs can be used when linking to pages within your own
website. They provide a shorthand way of telling the browser where to
find your files.

Email Links

mailto:
To create a link that starts up the user's email program and
addresses an email to a specified email address, you use the `<a>`
element. However, this time the value of the href attribute starts
with mailto: and is followed by the email address you want the
email to be sent to.

`<a href="mailto:jon@example.org">Email Jon</a>`

Example LINKS

`<html>`

   `<head>`
   
      `<title>Links</title>`
      
   `</head>`
   
      `<body>`
      
        `<h1 id="top">Film Folk</h1>`
        
        `<h2>Festival Diary</h2>`
        
         `<p>Here are some of the film festivals we`
         
            `will be attending this year.<br />Please`
            
            `<a href="mailto:filmfolk@example.org">`
            
                `contact us</a> if you would like more`
                
                                             `information.</p>`
                                             
        `<h3>January</h3>`
        
             `<p><a href="http://www.sundance.org">`
             
                           `Sundance Film Festival</a><br />`
                           
                                 `Park City, Utah, USA<br />`
                                 
                                      `20 - 30 January 2011</p>`
                                      
        `<h3>February</h3>`
        
           `<p><a href="http://www.tropfest.com">`
           
                                   `Tropfest</a><br />`
                                   
                              `Sydney, Australia<br />`
                              
                                     `20 February 2011</p>`
                `<!-- additional content -->`
                
           `<p><a href="about.html">About Film Folk</a></p>`
           
            `<p><a href="#top">Top of page</a></p>`
            
     `</body>`
     
`</html>`


***

## Layout

### Key Concepts in Positioning Elements

CSS treats each HTML element as if it is in its
own box. This box will either be a block-level
box or an inline box.
Block-level boxes start on a new line and act as the main building blocks
of any layout, while inline boxes flow between surrounding text. You can
control how much space each box takes up by setting the width of the
boxes (and sometimes the height, too). To separate boxes, you can use
borders, margins, padding, and background colors.

Containing Elements

If one block-level element sits inside another
block-level element then the outer box is
known as the containing or parent element.
It is common to group a number of elements together inside a `<div>`
(or other block-level) element. For example, you might group together
all of the elements that form the header of a site (such as the logo and
the main navigation). The `<div>` element that contains this group of
elements is then referred to as the containing element.

Controlling the Position of Elements

CSS has the following positioning schemes that allow you to control
the layout of a page: normal flow, relative positioning, and absolute
positioning. You specify the positioning scheme using the position
property in CSS. You can also float elements using the float property.

* Normal flow
Every block-level element
appears on a new line, causing
each item to appear lower down
the page than the previous one.
Even if you specify the width
of the boxes and there is space
for two elements to sit side-byside,
they will not appear next
to each other. This is the default
behavior (unless you tell the
browser to do something else).

* Relative Positioning
This moves an element from the
position it would be in normal
flow, shifting it to the top, right,
bottom, or left of where it
would have been placed. This
does not affect the position of
surrounding elements; they stay
in the position they would be in
in normal flow.

* Ab solute positioning
This positions the element
in relation to its containing
element. It is taken out of
normal flow, meaning that it
does not affect the position
of any surrounding elements
(as they simply ignore the
space it would have taken up).
Absolutely positioned elements
move as users scroll up and
down the page.

***

## Functions, Methods, and Objects

Browsers require very detailed instructions about what
we want them to do. Therefore, complex scripts can run
to hundreds (even thousands) of lines. Programmers use
functions, methods, and objects to organize their code.
This chapter is divided into three sections that introduce:

* FUNCTIONS & OBJECTS 
Functions consist of a series of statements that have been grouped together because they
perform a specific task. A method is the same as a function, except methods are created inside (and are
part of) an object.

* OBJECTS
* BUILT-IN OBJECTS

### WHAT IS A FUNCTION?

Functions let you group a series of statements together to perform a
specific task. If different parts of a script repeat the same task, you can
reuse the function (rather than repeating the same set of statements).

A BASIC FUNCTION

`var msg = 'Sign up to receive our newsletter for 10% off!';`
`function updateMessage() {`
`var el = document.getElementByld('message'};`
`el .textContent = msg;`
`}`
`updateMessage(};`


Calling functions

Defining a function does not execute it. Defining it names the function and specifies what to do when the function is called.


### 6 Reasons for Pair Programming

### Why pair program?

1. Greater efficiency
2. Engaged collaboration
3. Learning from fellow students
4. Social skills
5. Job interview readiness
6. Work environment readiness

[For More](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)
