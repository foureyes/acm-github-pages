---
layout: homework
title: "Assignment #1"
---

# Assignment #1 - Due Tuesday, Feb 2nd at 11PM

## Part 1 - Readings

Read __Chapter #1__, Introduction to Computers, Programs, and Java in your book, _{{site.book}}_

## Part 2 - Install Java and Eclipse

To develop Java applications, you'll have to install both the __Java Development Kit__, or JDK, as well as an integrated development environment, or IDE, called __Eclipse__ (you can, however, use any IDE that you're comfortable with).

The __JDK__ is a set of software that allows you to compile and run Java programs, and your IDE, Eclipse, is the application that you will use to actually _write_ programs.

Download and run the appropriate installers for your Operating System:

* [Java SE Development Kit 8  (JDK 8)](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
	* find the link for downloading the __JDK__
	* choose the appropriate installer for your OS and operating system 
* [Eclipse](https://eclipse.org/downloads/)
	* find the link for downloading "__Eclipse IDE for Java Developers__"
	* the download will be a compressed (zip) file
	* unzip/uncompress it in a directory of your choosing
	* go into the uncompressed folder (it should be named <code>eclipse</code>)
	* launch Eclipse

## Parts 3 and 4

(TO BE POSTED)

{% comment %}
## (20 points) Part 3 - Display Five Messages

* see section 1.12 in your book or [watch the video](http://www.cs.armstrong.edu/liang/intro9e/VideoNote/Eclipse/EclipseTutorial.htm) from the previous edition's supplemental material (may be slightly out-of-date, and a bit hokey!) for help with Eclipse
* create a new Java project in Eclipse 
* create a new class file called <code>DisplayFiveMessages</code>
* make sure the class name in your file matches (it _should_ if you're using Eclipse!) - <code>DisplayFiveMessages.java</code>
* follow the directions below (sourced from Chapter 1's Programming Exercises):

(Display five messages) Write a program that displays <code>Welcome to Java</code> five times. 

Example output:

<pre><code data-trim contenteditable>Welcome to Java
Welcome to Java
Welcome to Java
Welcome to Java
Welcome to Java
</code></pre>

* use consistent indentation, spacing and bracing style throughout your program
* add a comment that explains what the program does

## (30 points) Part 4 - Population Projection 

* create a new Java project in Eclipse
* create a new class file called <code>PopulationProjection</code>
* make sure the class name in your file matches (it _should_ if you're using Eclipse!) - <code>PopulationProjection.java</code>
* follow the directions below (sourced from Chapter 1's Programming Exercises):

(Population projection) The U.S. Census Bureau projects popopulation based on the following assumptions:

* One birth every 7 seconds
* One death every 13 seconds
* One new immigrant every 45 seconds

Write a program to display the population for each of the next five years. Assume the current population is 312,032,486 and one year has 365 days. Hint: In Java, if two integers perform division, the result is an integer. The fractional part is truncated. For example, 5/4 is 1 (not 1.25) and 10/4 is 2 (not 2.5). To get an accurate result with the fractional part, one of the values involved in the division must be a number with a decimal point. For example, 5.0/4 is 1.25 and 10/4.0 is 2.5.

* use consistent indentation, spacing and bracing style throughout your program
* add a comment that explains what the program does
{% endcomment %}

# Submission Process

* Submit assignment via NYU Classes
* Submit each <code>.java</code> file as a separate attachment
	* only submit .java files (do not submit .class files or any other files that are created in Eclipse)
	* you can find your .java files in the directory that you specified as your workspace... and within the project folder contained in the workspace directory


# Grading Criteria

(TO BE POSTED)
{% comment %}
* no credit: file does not compile
* -5 points: files and classes are not named according to instructions
* -5 points: inconsistent style using curly braces, inconsistent use of spaces and indentation, lack of comments
* -50% point value (approximately) of file: actual output of program does not match expected output
{% endcomment %}
