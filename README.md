# Website Performance Optimization portfolio project

This is Project #4 of the [Udacity Front-End Web Developer

## Goal
Optimize a website so that it achieves a target speed of 90 and runs at 60 frames per second.

## Getting started
The code for the "before" website can be found [here](https://github.com/udacity/frontend-nanodegree-mobile-portfolio)

## Requirement 1: Critical Rendering Path
Get index.html to a PageSpeed score for the mobile and desktop versions to at
least 90.

Suggested ways to fix the issues:

1. Optimize images
2. Eliminate render-blocking JS and CSS in above-the-fold content

Consider fixes:

1. Leverage browser caching
2. Enable compression
3. Minify HTML
4. Added media="print" after the href="style-print.css" so the browser does not block rendering.

### Optimize:

1. Optimize images: Google's PageSpeed tool provided two optimized images:
    * profilepic.jpg
    * pizzeria.jpg.
    * They were both sized and compressed. The original images file names were
    renamed with the suffix  "-lg".
2. To eliminate render-blocking JS & CSS, the following changes were made and implemented.
    * used a media query on the print.css. Now, it will only request the CSS
    file if screen = print
    * added async to the Google analytics script so it doesn't block rendering
    * moved the Google Analytics script to the bottom of the body so it doesn't
    block rendering
    * replaced the Google Font CSS file request to a JS script at the bottom of
    the body, so downloading the fonts won't block rendering
    * minified the css file.
