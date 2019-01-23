# Part 5: Data Integration, Normalization, and Publication
## Bringing it all together into one dataset

## Issues
- Common data anomalies and structural gaps from multi-source data integration
- Generating data for public consumption
- Working with multiple third-party libraries

## Practices
- Traversal of hierarchically-structured data
- Normalizing data to eliminate anomalies
- Denormalizing data to improve ease of use

## Data Integration Issues
### Shifting Requirements and Implementation Bugs
Maintaining any data repository is always a continuous undertaking. Just when you've got the process just like you want it ... somebody else does something to muck it up! Imagine if, for example, Fairfield University were to change the way it reports class schedules in Banner. We'd have to redo our Beautiful Soup scraper to accomodate, likely after discovering the change the hard way after a crash. 

Even if the data source has not changed, people are always coming up with new uses (and data formats) for data. In part 4, for example, we focused on getting course scheduling data but ignored enrollment data that might be of use later. The revised `course-schedules-beautiful-soup.py` module in the repo picks up this data by adding a just a few lines of code marked with the comment `# added 11/17/18`. We'll make use of that code in Part 6, when we go beyond course schedules and into course enrollments. 

### Design Bugs and Oversights
The most fundamental integration bugs actually arise in design, long before any code is written. There are three basic types:
- Data that is redundant and inconsistent
- Lack of relational data (keys, IDs, cross-references, etc.) needed to connect related datasets
- Lack of tracking logs or other history needed to diagnose processing errors and correct errors

While implementation bugs are more immediate -- a crash always gets your attention and often comes at the exactly the wrong momment -- design bugs are actually the harder ones to fix. It's like the difference between debugging syntax errors versus logic errors. Syntax errors can be detected by the Python interpretter, which even flags the exact line of code that triggered the error and provides a traceback to follow the error back to it's root cause. Logic errors are more subtle, leaving you to find them yourself, and often can't be fixed in a few lines of code. You may have to rewrite everything from scratch!

This tutorial focuses more on design than implementation, demonstrating a few practices one can employ to prevent logical errors in your data. 

## Data Publication with Legacy File Formats
In many respects, publishing data for mass consumption (e.g., as a web service) is where data analysis moves into data engineering. The focus is not on your analysis but on providing data to others who may have their own, novel uses for that data. It has to be provably right and stay right. 

Just for fun, we'll generate 1300+ class calendars in iCal format, ready to import into your phone. Then perhaps we could design a web service (in Flask, perhaps?) to let people search and subscribe to these calendars, but that would be beyond the scope of this course. However, the purpose here is to put our data to the test: can we generate internet-standard course calendars from our data? If we can do that then we can truly say that we understand the data in enough detail to be useful. 

## The Profusion of Third-party Libraries
One of the most confusing aspects of data analysis in the modern world is the shear volume and complexity of the software available. In the dinosaur days we used to program most things from scratch. (Just the other day I came across Pascal code from my undergraduate thesis that would look earily familiar to an MS BA student: T tests, Chi-Square tests, randomized sampling for cross-validation, etc.) Now, however, there is lots of code to do these things, complete with source code on GitHub! So, instead of writing code with a white sheet of paper (literally sometimes), you instead stitch code from multiple sources together to do the dirty work. However, how do you choose the code? And what if multiple libraries claim to do the same thing but in slightly different (and incompatible) ways? 

In this tutorial we will mix and match several libraries for working with dates, calendars, and file formats. 


