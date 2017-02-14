---
layout: homework
title: "Processing Installation"
---


## Processing

### Creating a Processing Program

#### Overview

We'll be using a library called [Processing](https://processing.org/) to integrate graphics and processing into our programs. Try setting up a processing project / file... and use the demo code below to test out your setup.

#### Setup

About your class file:

* Create a class (<code>.java</code>) file called <code>ProcessingDemo.java</code>
* (This can be within a project that contains the other parts of this homework or it can be in separate project on its own)

Read up on processing:

* [https://processing.org/tutorials/eclipse/](https://processing.org/tutorials/eclipse/)
* [https://processing.org/examples/setupdraw.html](https://processing.org/examples/setupdraw.html)
* [https://processing.org/examples/shapeprimitives.html](https://processing.org/examples/shapeprimitives.html)

Adding the processing library to your project

* [Download core.jar](../resources/jars/core.jar), the core processing library
* Import into Eclipse by:
	1. Clicking on your project in the project navigator
	1. <code>File</code> &rarr; <code>Import</code>
	1. Choose <code>General</code> &rarr; <code>File System</code>
	1. Click on <code>Browse</code>... and go to the folder where you downloaded <code>core.jar</code>
	1. Click the checkbox next to the folder to make sure that the folder and core.jar have checks next to them
	1. Expand your project in the project navigator 
	1. You should see <code>core.jar</code>
	1. Right click on <code>core.jar</code>
	1. Choose <code>Build Path</code>
	1. Choose <code>Add to Build Path</code>


<video markdown="block" preload controls>
<source src="../resources/video/eclipse-processing-2.ogv" />
<source src="../resources/video/eclipse-processing-2.webm" />
</video>

### Features

Use the following code in your <code>.java</code> file:

<pre><code data-trim contenteditable>import processing.core.*; 

public class ProcessingDemo extends PApplet{
    public static void main(String[] args) {
        PApplet.main("ProcessingDemo");
    }

    // hey. we've seen multidimensional arrays before!
    // this will store our coordinates, as well as velocity
    int[][] coords = new int[1000][4];
    public static final int WIDTH = 640, HEIGHT = 480;
    public static final int MAX_DX = 3, MAX_DY = 3;
    
    // cheap way to make indexes more readable
    public static final int X = 0, Y = 1, DX = 2, DY = 3;
    
    // called once
    public void setup() {
        size(WIDTH, HEIGHT); 
        frameRate(30);
        fill(coords);
    }

    // called repeatedly
    public void draw() { 
         background(0);
         for(int i = 0; i < coords.length; i++) {
             ellipse(coords[i][X], coords[i][Y], 3, 3);
             coords[i][X] += coords[i][DX];
             coords[i][Y] += coords[i][DY];
             if(coords[i][X] > WIDTH) {
                 coords[i][X] = 0;
             }
             if(coords[i][Y] > HEIGHT) {
                 coords[i][Y] = 0;
             }           
         }
    }
    
    public static void fill(int[][] arr) {
        for(int i = 0; i < arr.length; i++) {
            arr[i][X] = (int) (Math.random() * WIDTH) + 1;
            arr[i][Y] = (int) (Math.random() * HEIGHT) + 1;
            arr[i][DX] = (int) (Math.random() * MAX_DX) + 1;    
            arr[i][DY] = (int) (Math.random() * MAX_DY) + 1;    
        }
    }
}

</code></pre>

#### Example Output:

<div markdown="block" class="img">
![gifs plz](../resources/img/processing-demo.gif)
</div>



