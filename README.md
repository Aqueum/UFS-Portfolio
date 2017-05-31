# UFS-Portfolio
- Udacity Full Stack - Portfolio
- [Udacity Full Stack Web Developer Nanodegree](
https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004) 
- Martin Currie (Aqueum) - 31 May 2017

# Getting Started
1. Ensure all the files listed under 'Files' below are in the same folder
(click clone or download in [this](https://github.com/Aqueum/UFS-Portfolio) 
& follow instructions)
2. Open Index.html in one of the following browsers:
- Chrome 21+
- Sarafi 6.1+
- Firefox 22+
- Opera 12.1+
- Internet Explorer 11+
- Android 4.4+
- iOS Safari 7.1+
- Blackberry 10+

Limited compatibility is due to use of [Flexbox](
https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

# How to create your own portfolio
Edit the JaneDoette2.html file's h1, h3, h4, a & p tags

# Known issues
## Fonts on JaneDoette2
`strings design-mockup-portfolio.pdf | grep FontName`
yields
`<< /Type /FontDescriptor /FontName /OYETYJ+OpenSans /Flags 4 /FontBBox 
[-550 -271 1204 1048]`
so I used google's OpenSans, but looking at the upper case J's this clearly
isn't quite right.

The overlapping font set given when entering images of "Jane Doette" and 
"Featured Work" into WhatTheFont was SmytheSans (thin & regular respectively)
but these aren't available at reasonable cost for a MOOC...

## Font Sizes on JaneDoette2
After being taught mobile first, my second attempt employed this methodology.
As I couldn't find a way to wrap or otherwise shrink urls (`.worklink 
{white-space: nowrap; overflow: hidden; text-overflow: ellipsis; min-width: 
10px;}` didn't work), I was forced to select too small a font size in order 
to stop long URLs from resulting in uneven image sizes.  I feel this was an 
acceptable compromise given the following mitigation.

In order to mitigate the potential small tap target issue, I added links to the
images.  (I tried adding links to the entire article but this led to 
underlining of the headings which `h3 {text-decoration: none;}` would not 
resolve.)

## Passing Variables
I don't like defining the same variable at multiple points in a document 
so I tried using CSS variables, but got rid of them at the request of the 
CSS Style checker.

I feel that as a style element, the swatch colours should be defined in CSS, 
therefor the text describing the swatch colours should also come from the CSS
variable, however, while I can pass text using ::after, I couldn't seem to find 
a way to pass variables:
`.corporate::after {content: var(--corporate);}` 
doesn't work.

I was concerned that CSS variables are still an 'experimental technology' so 
wouldn't use it in a production site, but assumed that Udacity reviewers would 
have up to date browsers...  Is there a more stable means of passing variables
 in CSS, or a way to prefix this?
Either way, I lost them at the request of: 
https://jigsaw.w3.org/css-validator/#validate_by_input
 
## Prefixing
CSS is still to be prefixed, is this something we should do with all flex CSS?

# Files
## Index.html
The front page for my Udacity portfolio

## JaneDoette2.html
The HTML intended to match (but mobile first) design-mockup-portfolio.pdf

## css/JaneDoette2.css
The stylesheet intended to match (but mobile first) design-mockup-portfolio.pdf

## css/Portfolio.css
The stylesheet for my Udacity portfolio

## design-mockup-portfolio.pdf
The original brief, to be emulated (but mobile first) in this exercise.

## img/[X].svg 
where [X] =
Applify, Bokeh, Sunflower, html-banner, JaneDoetteSite, JaneDoettePDF, Movies
Various screen-grabbed cropped and web optimised image files
to give <200kB file sizes (<100kb for thumbnails)

## img/ Aqueum-Banner-5D3A1934-[X]x[Y].jpg, Martin-Currie-5D3A9026-100x100.jpg
Original photographs copyright Martin Currie, Andeye 2012

## img/udacity.svg
Udacity logo taken from https://worldvectorlogo.com/logo/udacity

## img/ Photography.svg, Water.svg, Code.svg
Vector files I created in Affinity Designer for this project

## JaneDoette.html & JaneDoette.css
The original files from my first attempt, I found moving the swatches below the
header's bar to be such a major structural change and the CSS had become so 
muddled that I abandoned these, restructured the HTML to JaneDoette2.html and 
started the CSS from scratch in JaneDoette2.css


# Contributing
This is an assessed project, so I'd probably get in trouble for accepting 
external input...

# Code Status
Can Udacity add a badge here..?

# License
Images and artwork are subject to copyright, all rights reserved. 
The code, you're welcome to under GNU v3.0, 
but unfortunately images cannot be shared.
