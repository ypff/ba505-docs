# Part 4: HTML Scraping and JSON generation with Beautiful Soup
## Issues Covered
* Introduction to Beautiful Soup, a full featured framework for parsing HTML text.

## Practices Demonstrated
* Incremental development, writing and code in small, testable steps
* Basic Beautiful Soup usage to parse tabular data embedded in a web page
* Packaging code into an importable module

## Learn About Beautiful Soup
[Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/) is the defacto standard for scraping HTML data in Python. 
> Beautiful Soup is a Python library designed for quick turnaround projects like screen-scraping. Three features make it powerful:
> 
>Beautiful Soup provides a few simple methods and Pythonic idioms for navigating, searching, and modifying a parse tree: a toolkit for dissecting a document and extracting what you need. It doesn't take much code to write an application
>Beautiful Soup automatically converts incoming documents to Unicode and outgoing documents to UTF-8. You don't have to think about encodings, unless the document doesn't specify an encoding and Beautiful Soup can't detect one. Then you just have to specify the original encoding.
>Beautiful Soup sits on top of popular Python parsers like lxml and html5lib, allowing you to try out different parsing strategies or trade speed for flexibility.
>Beautiful Soup parses anything you give it, and does the tree traversal stuff for you. You can tell it "Find all the links", or "Find all the links of class externalLink", or "Find all the links whose urls match "foo.com", or "Find the table heading that's got bold text, then give me that text."
>
>Valuable data that was once locked up in poorly-designed websites is now within your reach. Projects that would have taken hours take only minutes with Beautiful Soup.

If you do nothing else, at least read through the [Quick Start docs](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#quick-start), which gives examples and instructions for everyday tasks. Everything shown in the tutorial is based on the Quick Start.

## Get the code
Fork and clone the code from [GitHub Classroom](https://classroom.github.com/a/bwtxQ6Ca). 

## Try it out for yourself
In JupyterLab, run the `Part4.ipynb` notebook one cell at a time. Don't just rush through. It's important to read (study!!!) the code. Pay attention to how the code morphs from one cell to the next. That is how you should approach your Final projects. Treat the code as a living document that grows and mutates as you work on it.   

