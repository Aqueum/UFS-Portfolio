# UFS-Portfolio
- Udacity Full Stack - Portfolio
- [Udacity Full Stack Web Developer Nanodegree](
https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004) 
- Martin Currie (Aqueum) - 31 May 2017

# Getting Started
1. Ensure all the files listed under 'Files' below are in the same folder
(click clone or download in [this](https://github.com/Aqueum/UFS-Portfolio) 
& follow instructions)
2. Open JaneDoette2.html in a browser as least as new as:
- Chrome 49.0
- Edge (Internet Explorer NOT supported)
- Firefox 31
- Opera 36.0
- Safari (WebKit) 9.1
- Android Webview 49.0 (Android NOT supported)
- Firefox Mobile (Gecko) 29
- Safari Mobile 9.1
- Chrome for Android 49.0

Limited compatibility is due to use of [CSS variables](
https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_variables) - see 
 passing variables, below.

# How to create your own portfolio
Edit the JaneDoette2.html file's h1, h3, h4, a & p tags

# Known issues
## Fonts
`strings design-mockup-portfolio.pdf | grep FontName`
yields
`<< /Type /FontDescriptor /FontName /OYETYJ+OpenSans /Flags 4 /FontBBox 
[-550 -271 1204 1048]`
so I used google's OpenSans, but looking at the upper case J's this clearly
isn't quite right.

The overlapping font set given when entering images of "Jane Doette" and 
"Featured Work" into WhatTheFont was SmytheSans (thin & regular respectively)
but these aren't available at reasonable cost for a MOOC...

## Font Sizes
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
I don't like defining the same variable at multiple points in a document and 
feel that as a style element, the swatch colours should be defined in CSS, 
therefor the text describing the swatch colours should also come from the CSS
variable, however, while I can pass text using ::after, I can't seem to find a
way to pass variables:
`.corporate::after {content: var(--corporate);}` 
doesn't work

# Files
## JaneDoette2.html
The HTML intended to match (but mobile first) design-mockup-portfolio.pdf

## css/JaneDoette2.css
The stylesheet intended to match (but mobile first) design-mockup-portfolio.pdf

## design-mockup-portfolio.pdf
The original brief, to be emulated (but mobile first) in this exercise.

## img/[various].jpg
Various files lifted in photoshop from the PDF then cropped and web optimised
to give <200kB file sizes (<100kb for thumbnails)

## img/udacity.svg
Udacity logo taken from https://worldvectorlogo.com/logo/udacity

## JaneDoette.html & JaneDoette.css
The original files from my first attempt, I found moving the swatches below the
header's bar to be such a major structural change and the CSS had become so 
muddled that I abandoned these, restructured the HTML to JaneDoette2.html and 
started the CSS from scratch in JaneDoette2.css


# Contributing
This is an assessed project, so I'd probably get in trouble for accepting 
external input.
Feel free to fork as long as you're not using this as part of your own 
coursework.

# Code Status
Can Udacity add a badge here..?

# License
See [LICENSE](https://github.com/Aqueum/UFS-Portfolio/blob/master/LICENSE)

