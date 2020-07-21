Robin Weiland


ECG Summary
==================

[TOC]

<div style="page-break-after: always; break-after: page;"></div>

# 01 Game Engine Design

---

|                Game logic                |                 Data                 |                         Game Engine                          |
| :--------------------------------------: | :----------------------------------: | :----------------------------------------------------------: |
| algorithms realizing<br />the game rules | various data used<br />by the engine | other algorithms, "independent"<br />of the game logic and data |

## Game engine components

<img src="C:\Users\robin\Documents\Uni\2. Semester\ECG\Dokumentation\Template\res\engine-components.png" alt="engine components" style="zoom:60%;" align="left" />

## Game Engine Data

-   ==Media assets== geometric models, textures, animations, sounds
-   ==Level data== objects in a level and how they interact
-   ==Object configuration data== physical properties and behavior control data
-   ==User Interface configuration data== types of input devices and their mapping
-   ==Engine configuration data== drivers, resolution, ...

<div style="page-break-after: always; break-after: page;"></div> 

# 02 Geometry

---

## Geometric objects

-   characters, items, props, game levels, ...
-   Usually created via **geometric modelling tools** ([blender](https://www.blender.org/about/), [maya](https://www.autodesk.com/products/maya/features), ...)
-   Modelling:
    -   **shape modelling:** shape representation by placing _geometric primitives_
    -   **appearance modelling:** material properties like color, reflection properties, textures, etc.

## Geometric model representation

>   Models are polygonal approximations of continuous objects.

## Polygons

-   **points**, typically in 3D-space $(\R^3)$, represented by $x/y/y$-coordinates, called **vertex**

-   **valence**: number of adjacent vertices of a given vertex

-   **edges**, line segments connecting two **vertices**

-   **polygon**, interior of a closed planar connected series of line segments

    (edges do not cross each other and each vertex is connected with exactly two edges)

## Polygon mesh

-   Surface composed of polygons (**faces**)
-   **Hollow**, if mesh is not closed

## Polygonal approximation

- Approximation of a continuous surface by a polygon mesh.
- Typically consists of a **discrete set of points** of the continuous connected via edges.
- Constructing the connectivity (edges) for a given set of
  points is called **triangulation**.
- Usually **adaptive**: more/smaller polygons $\longrightarrow$ regions with high **curvature**

## Mesh storage / representation

-   **Geometry** vertices' location in 3D-space
-   **Topology** connection of vertices & polygons

### Explicit representation 

Store three vertices for each of the $F$ triangles: $F * 3 * 3 = 9F \quad floats$ (**high redundancy**)

<img src="res\explicit-geometric-representation.png" alt="explicit geometric representation" style="zoom:60%;" align="left"/>



### Triangle Mesh representation

-   **Shared vertex** ("indexed face set") representation
-   Used in e.g.  [*.obj*](https://en.wikipedia.org/wiki/Wavefront_.obj_file), [*.off*](https://en.wikipedia.org/wiki/OFF_(file_format)) files
-   Array of all vertices (3V floats)
-   Array of triangles with indices into the vertex list (3F integers)

<img src="res\triangle-mesh-representation.png" alt="triangle mesh representation" style="zoom:60%;" align="left"/>

## Procedural Modelling

>   Number of techniques to **automatically** create 3D models and textures from sets of rules

Example: sphere generation after trigonometric rules.

### Procedural terrain modelling

<img src="res\procedural-terrain.png" alt="procedural terrain" style="zoom:60%;" align="left"/>

-   Generate a random 2D "density field" and interpret values as height values over a 2D domain
<img src="res\density-field.png" alt="density field" style="zoom:60%;" />
-   Draw field as height field

<div style="page-break-after: always; break-after: page;"></div>

==TODO== diamond square algorithm