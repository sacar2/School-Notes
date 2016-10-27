# 07: Mesh Data Structures

* Model anything with arbitrary precision

* Easy to build and modify

* Efficient computations


* flexible

* rendered quickly

* most modern 3D models are textured polygon models

* polygons are planar, can only approximate curved surfaces with _many_ polygons


## 3D Modeling

* **Points: **2D range image\/\/3D point cloud
* **Solids**: voxels\/solid geometry
* **Surfaces: **polygonal mesh, parametric surface, subdivision surfaces, implicit surfaces
* **Procedural**: particle system, fractal

## Range Data

* **Range Image: **pixel location \(r,c\), pixel contains depth \(not colour\)
* **3D point cloud: **set of points in 3D space \(xi. yi. zi\)

## Representing Polygonal Meshes

### Simple \(but dumb\)

* float triangle\[n\]\[3\]\[3\]
* redundant: each vertex stored multiple times

### Vertex List, Face List

* List of vertices \(only vertex coordinates\)
* List of Triangles, each triple of vertex id's \(O\(F\) time for F faces\)

### Fancier Schemes

* store more topological info

* Adjacency queries answered in O\(1\) time


## **Properties of Meshes**

polygons b\/c simple to represent and manipulate, approximate smooth surfaces, each planarpolygon has a unique normal
* **Solidity**: A mesh represents a solid object if its faces together enclose a finite amount of space.
* **Connectedness**: A mesh is connected if every face shares at least one edge with some other face.
* **Simplicity**: A mesh is simple if the object it represents is solid and has no holes through it.
* **Planarity**: A mesh is planar if every face is a planar polygon.
* **Convexity**: A mesh is **convex** if the line connecting any two points within the object lies wholly inside the mesh object.

## Mesh Triangulation

### Voronoi Diagram

> Subdivision of the plane where the faces correspond to the regions where one site is closest

Given some trees, which region will they occupy? Given ambulance posts in a country, in case of an emergency somewhere, where should the ambulance come from? 

![](/assets/voronoi.png)

### Delaunay Triangulation

Straight line embedding of the dual graph G

![](/assets/delunay.png)

## Mesh Simplification

* need for accuracy depends on the application 

* storage efficiency

* faster rendering

* simpler manipulation


![](/assets/mesh simplification.png)
### Vertex Clustering 

* partition space into cells \(grids, spheres, octrees, etc.\) 

* merge all vertices within the same cell

* general & robust, but not best quality


![](/assets/vertex clustering.png)
### Mesh Retiling 

* Resample mesh with “uniformly spaced” random vertices 

* triangulate the new vertices

* slow, blurs the sharp features


![](/assets/mesh retiling.png)
### Mesh Decimation

![](/assets/mesh decimation.png)

## Mesh Data Structure

![](/assets/mesh data structure.png)

## Half Edge Data Structure

![](/assets/half edge data structure.png)

## Surface of Revolution

![](/assets/surfaces of revolution.png)



