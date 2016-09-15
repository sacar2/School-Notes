#CS 3388 Notes

##Table of Contents

- [01: Intro to Computer Graphics](#01:-intro-to-computer-graphics)
	- [Setting Up in XCode](#setting-up-in-xcode)
- [02: OpenGL Basics](#02-openGL-basics)
- [03: Bresenham's Algorithms](#03:-bresenham's-algorithms)
- [04: Geometric Transformations](#04-geometric-transformations)
- [05: Viewing and Projections](#05-viewing-projections)
- [06: Clipping](#06-clipping)
- [07: Mesh Data Structures](#07-mesh-data-structures)
- [08: Curve and Surface Design](#08-curve-and-surface-design)
- [09: Lightning Models](#09-lightning-models)
- [10: Ray Tracing](#10-ray-tracing)
- [11: Fractals](#11-fractals)


#01: Intro to Computer Graphics

##Setting Up in XCode
- Create new Command Line Tool
- Click on your project name then click on *Build Phases*

Link Frameworks:
- Click ‘*Link Binary With Libraries*’
- Click the + button
- Type *OpenGL* in the search box, Click *OpenGL.framework*, then click *Add*
- Click the + button again
- Type *glut* in the search box, Click *GLUT.framework*, then click *Add* 

Remove Depreciation Warnings (GLUT OpenGL files have been depreciated)
- Click the *Build Settings* tab
- In the search bar on the top right of the tab, type *deprecated*
- Under *Apple LLVM – Warnings – All Languages*, look for “*Deprecated Functions*” setting
- Change the setting to “No”

Include libraries in your project
- select main.c
- add the following files:
```#include <OpenGL/gl.h>
#include <OpenGL/glu.h>
#include <GLUT/glut.h>```
Done!


#02: OpenGL Basics
#03: Bresenham's Algorithms
#04: Geometric Transformations
#05: Viewing and Projections
#06: Clipping
#07: Mesh Data Structures
#08: Curve and Surface Design
#09: Lightning Models
#10: Ray Tracing
#11: Fractals
