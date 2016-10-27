**Primitive types**

it is advised to use the primitive types defined by OpenGL. Instead of writing`float` we prefix it with `GL`; the same holds for `int`, `uint`, `char`, `bool` etc. 

OpenGL defines the memory-layout of their GL primitives in a cross-platform manner since some operating systems may have different memory-layouts for their primitive types. Using OpenGL's primitive types helps to ensure that your application works on multiple platforms.

