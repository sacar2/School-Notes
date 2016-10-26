# Setting Up In XCode

* Create new Command Line Tool

# GLUT

### Link Frameworks:

* Click on your project name then click on _Build Phases_
* Click ‘_Link Binary With Libraries_’
* Click the + button
* Type _OpenGL_ in the search box, Click _OpenGL.framework_, then click _Add_
* Click the + button again
* Type _glut_ in the search box, Click _GLUT.framework_, then click _Add_ 

### Remove Depreciation Warnings \(GLUT OpenGL files have been depreciated\)

* Click the _Build Settings_ tab
* In the search bar on the top right of the tab, type _deprecated_
* Under _Apple LLVM – Warnings – All Languages_, look for “_Deprecated Functions_” setting
* Change the setting to “No”

### Include libraries in your project

* select main.c
* add the following files:

```c++
#include <OpenGL/gl.h>
#include <OpenGL/glu.h>
#include <GLUT/glut.h>
```

Done!

# GLFW

## Downloading GLFW & GLEW

1. download GLFW & GLEW
2. unzip both
3. create new project - your base OpenGL project
4. put GLEW & GLFW inside new project folder
5. create 'build' folder inside `glfw` folder
6. Open CMake. input GLFW location, and put output as `glfw/build` folder
7. Open newly created GLFW project in `glfw/build`
  1. change the scheme ALL\_BUILD to "install" 
  2. Click the Run button.

8. Open terminal, cd to GLEW folder, "`sudo make install`"
  1. GLEW libraries are now in `glew/lib`, and GLEW include files are in `glew/include`

9. Open your base OpenGL project &gt; Build Phases &gt; Link Binary w\/ libraries:
  1. OpenGL.framework
  2. libGLEW. ------, in `/usr/local/lib`
  3. libglfw. -------, in ... look for it...

10. Go to Build settings&gt; search paths&gt; 
  1. HEADER search paths: \/usr\/local\/include
  2. LIBRARY Search paths: \/usr\/local\/lib

11. Still under Build settings, go to Linking&gt; Other Linker Flags, add `-lGLEW`
12. \#include &lt;GL\/glew.h&gt; 
13. \#include &lt;GLFW\/glfw3.h&gt;


## Adding GLFW & GLEW To Your Project

1. Create new project
2. Copy and paste GLFW & GLEW folders from base project
3. Open your OpenGL project &gt; Build Phases &gt; Link Binary w\/ libraries: 
  1. OpenGL.framework 
  2. libGLEW. ------, in `/usr/local/lib` 
  3. libglfw. -------, in ... look for it...

4. Go to Build settings&gt; search paths&gt; 1. HEADER search paths: \/usr\/local\/include 2. LIBRARY Search paths: \/usr\/local\/lib
5. still under Build settings, go to Linking&gt; Other Linker Flags, add `-lGLEW`
6. \#include &lt;GL\/glew.h&gt;
7. \#include &lt;GLFW\/glfw3.h&gt;

