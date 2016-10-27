# 07: Mesh Data Structures

* Model anything with arbitrary precision 

* Easy to build and modify

* Efficient computations


+ flexible

+ rendered quickly

+ most modern 3D models are textured polygon models

- polygons are planar, can only approximate curved surfaces with _many_ polygons

## 3D Modeling

* **Points: **2D range image\/\/3D point cloud
*  **Solids**: voxels\/solid geometry
* **Surfaces: **polygonal mesh, parametric surface, subdivision surfaces, implicit surfaces
* **Procedural**: particle system, fractal

## Range Data

* **Range Image: **pixel location \(r,c\), pixel contains depth \(not colour\)
* **3D point cloud: **set of points in 3D space \(xi. yi. zi\)



## **Properties of Meshes**

* **Solidity**: A mesh represents a solid object if its faces together enclose a finite amount of space.
* **Connectedness**: A mesh is connected if every face shares at least one edge with some other face.
* **Simplicity**: A mesh is simple if the object it represents is solid and has no holes through it.
* **Planarity**: A mesh is planar if every face is a planar polygon.
* **Convexity**: A mesh is **convex** if the line connecting any two points within the object lies wholly inside the mesh object.




