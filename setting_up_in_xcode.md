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

1. download GLFW & GLEW

2. unzip both

3. create new project 

4. put GLEW & GLFW inside new project folder

5. create 'build' folder inside `glfw` folder

6. using CMake, input GLFW location, and put output as `glfw/build` folder

7. open newly created GLFW project in `glfw/build`, and build the project

8. open terminal, cd to GLEW folder, "`sudo make install`"

  1. GLEW libraries are now in `glew/lib`, and GLEW include files are in `glew/include`



