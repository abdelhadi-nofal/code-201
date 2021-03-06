## Images 

### HTML `<img>` Tag

Definition and Usage
The `<img>` tag is used to embed an image in an HTML page.

Images are not technically inserted into a web page; images are linked to web pages. The <img> tag creates a holding space for the referenced image.

The `<img>` tag has two required attributes:

src - Specifies the path to the image
alt - Specifies an alternate text for the image, if the image for some reason cannot be displayed
Note: Also, always specify the width and height of an image. If width and height are not specified, the page might flicker while the image loads.

Tip: To link an image to another document, simply nest the `<img>` tag inside an <a> tag (see example below).

### Attributes

Global Attributes

The `<img>` tag also supports the Global Attributes in HTML.

Event Attributes

The <img> tag also supports the Event Attributes in HTML.


## JPEG vs PNG vs GIF — which image format to use and when?

There are hundreds of image formats available each with a specific use case. I bet most of us wouldn’t have come across 90% of the image formats listed on Wikipedia.
In this post, we would only be looking at the three most commonly used image formats in websites and mobile applications — JPEG, PNG and GIF. Several statistics reports, including the one from HTTP Archive, indicate that these 3 formats together comprise of more than 95% of all images loaded on websites. However, these 3 image formats have significant differences amongst themselves thus making each of them suitable for specific use cases. Understanding these major differences would help us deliver the best possible images to our website and mobile app users.
TL;DR
Use JPEG format for all images that contain a natural scene or photograph where variation in colour and intensity is smooth. Use PNG format for any image that needs transparency or for images with text & objects with sharp contrast edges like logos. Use GIF format for images that contain animations.
Compression
Almost all forms of data that we see on the internet — text, image, video etc. — are compressed to reduce the size of data and ensure faster transmission. Choosing the correct format and compression is a major factor that determines image size.
Compression can be of two types — lossless and lossy. In lossless compression, it is possible to reconstruct the original image from the compressed image because there is no information loss during compression. This is not the case in lossy compression i.e. data loss in lossy compression is irreversible. Lossy compression algorithms always have a superior compression ratio (the ratio of size of compressed image to original image) as compared to lossless compression. However, this compression ratio comes at a cost of reduced quality that becomes more evident after zooming in on the image. This noticeable reduction in quality or distortion of the image is called compression artefact.
JPEG is a lossy compression specification that takes advantage of human perception. It can achieve compression ratios of 1:10 without any perceivable difference in quality. Beyond this, the compression artefacts become more prominent. Because JPEG compression works by averaging out colours of nearby pixels (read Discrete Cosine Transform), JPEG images are best suited for photographs and paintings of natural scenes where the variations in colour and intensity are smooth. However, if an image contains text or lines, where a sharp contrast between adjacent pixels is desired to highlight the proper shape, this lossy compression technique does not yield good results.

For more vist [LINK](https://blog.imagekit.io/jpeg-vs-png-vs-gif-which-image-format-to-use-and-when-c8913ae3e01d)

***

## HTML color codes and names

color

The color property allows you
to specify the color of text inside
an element. You can specify any
color in CSS in one of three ways:

rgb values
example: rgb(100,100,90)

hex codes
example: #ee3e80

color names
There are 147 predefined color
names that are recognized
by browsers. For example:
DarkCyan

Background Color

CSS treats each HTML element
as if it appears in a box, and the
background-color property
sets the color of the background
for that box.
You can specify your choice of
background color in the same
three ways you can specify
foreground colors: RGB values,
hex codes, and color names
(covered on the next page).

Understanding Color

Every color on a computer screen is created by mixing amounts of red,
green, and blue. To find the color you want, you can use a color picker.

Contrast

When picking foreground and background
colors, it is important to ensure that there is
enough contrast for the text to be legible.

CSS 3: HSL Colors

CSS3 introduces an entirely new and intuitive
way to specify colors using hue, saturation,
and lightness values.

hue
Hue is the colloquial idea of
color. In HSL colors, hue is often
represented as a color circle
where the angle represents the
color, although it may also be
shown as a slider with values
from 0 to 360.

saturation
Saturation is the amount of
gray in a color. Saturation is
represented as a percentage.
100% is full saturation and 0%
is a shade of gray.

lightness
Lightness is the amount of
white (lightness) or black
(darkness) in a color. Lightness
is represented as a percentage.
0% lightness is black, 100%
lightness is white, and 50%
lightness is normal. Lightness
is sometimes referred to as
luminosity.

CSS 3: HSL & HSLA

The hsl color property has
been introduced in CSS3 as an
alternative way to specify colors.
The value of the property starts
with the letters hsl, followed
by individual values inside
parentheses for:

hue
This is expressed as an angle
(between 0 and 360 degrees).

saturation
This is expressed as a
percentage.

lightness
This is expressed as a
percentage with 0% being white,
50% being normal, and 100%
being black.


***

### Text

Typeface Terminology

Serif

Serif fonts have extra details on
the ends of the main strokes of
the letters. These details are
known as serifs.

Sans-Serif

Sans-serif fonts have straight
ends to letters, and therefore
have a much cleaner design.

Monospace

Every letter in a monospace (or
fixed-width) font is the same
width. (Non-monospace fonts
have different widths.)

Choosing a Typeface for your Website

When choosing
a typeface, it
is important to
understand that a
browser will usually
only display it if it's
installed on that
user's computer.

Serif

Serif fonts have extra details on
the end of the main strokes of
the letters.

Sans-Serif

Sans-serif fonts have straight
ends to letters and therefore
have a much cleaner design.

Monospace

Every letter in a monospace
typeface is the same width.
(Non-monospace fonts have
different widths.)

Cursive

Cursive fonts either have
joining strokes or other cursive
characteristics, such as
handwriting styles.

Fantasy

Fantasy fonts are usually
decorative fonts and are often
used for titles. They're not
designed for long bodies of text.

Specifying Typefaces

font-family
The font-family property
allows you to specify the
typeface that should be used for
any text inside the element(s) to
which a CSS rule applies.
The value of this property is the
name of the typeface you want
to use.
The people who are visiting
your site need the typeface you
have specified installed on their
computer in order for it to be
displayed.

font-size
The font-size property enables
you to specify a size for the
font. There are several ways to
specify the size of a font. The
most common are:
pixels
Pixels are commonly used
because they allow web
designers very precise control
over how much space their text
takes up. The number of pixels is
followed by the letters px.
percentages
The default size of text in
browsers is 16px. So a size of
75% would be the equivalent of
12px, and 200% would be 32px.
If you create a rule to make all
text inside the <body> element
to be 75% of the default size (to
make it 12px), and then specify
another rule that indicates the
content of an element inside the
<body> element should be 75%
size, it will be 9px (75% of the
12px font size).
ems
An em is equivalent to the width
of a letter m.

Type Scales

You may have noticed that programs such as
Word, Photoshop and InDesign offer the same
sizes of text.

UpperCase & LowerCase

text-transform
The text-transform property
is used to change the case of
text giving it one of the following
values:

uppercase
This causes the text to appear
uppercase.

lowercase
This causes the text to appear
lowercase.

capitalize
This causes the first letter of
each word to appear capitalized.

text-decoration
The text-decoration property
allows you to specify the
following values:
none
This removes any decoration
already applied to the text.
underline
This adds a line underneath the
text.
overline
This adds a line over the top of
the text.
line-through
This adds a line through words.
blink
This animates the text to make it
flash on and off (however this is
generally frowned upon, as it is
considered rather annoying).

text-align

The text-align property allows
you to control the alignment of
text. The property can take one
of four values:
left
This indicates that the text
should be left-aligned.
right
This indicates that the text
should be right-aligned.
center
This allows you to center text.
justify
This indicates that every line in
a paragraph, except the last line,
should be set to take up the full
width of the containing box.


***

