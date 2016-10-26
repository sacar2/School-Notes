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



