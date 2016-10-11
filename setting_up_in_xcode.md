# Setting Up In XCode
- Create new Command Line Tool

###Link Frameworks:
- Click on your project name then click on *Build Phases*
- Click ‘*Link Binary With Libraries*’
- Click the + button
- Type *OpenGL* in the search box, Click *OpenGL.framework*, then click *Add*
- Click the + button again
- Type *glut* in the search box, Click *GLUT.framework*, then click *Add* 

###Remove Depreciation Warnings (GLUT OpenGL files have been depreciated)
- Click the *Build Settings* tab
- In the search bar on the top right of the tab, type *deprecated*
- Under *Apple LLVM – Warnings – All Languages*, look for “*Deprecated Functions*” setting
- Change the setting to “No”

###Include libraries in your project
- select main.c
- add the following files:

```c++
#include <OpenGL/gl.h>
#include <OpenGL/glu.h>
#include <GLUT/glut.h>
```

Done!