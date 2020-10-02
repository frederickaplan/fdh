---
title: 'Foundations in Digital Humanities 2.6'
subtitle: '3D Models and Measures'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# 3D Models and Measures

## Concepts

Modelling vs Sampling : 

### Modelling

Model-based Procedural methods. Architectural grammars. Class I and Class II elements. The question of realism. (maybe moved to part 3)

### Sampling

Acquisition techniques : 

- Different methods : Lidar, Time of Flight
- Finding a compromise between time and precision. 
- Using standard camera or dedicated scanners (for instance LIDAR)
- Iterated Scanning
- Visualisation of the scans



Principles of Phtogrammetry. 

Homologous Points. Odometry. Desification. Adjacent graph. 

Calibration

Evaluation of precision of models

#### Cloud Points

Problems with cloud points

- Monolitics 
- Difficulty of manipulation, store, manage, compare. 
- Do not comply with some of cadastral requierement 
- Nice to have but not necessary. 

The between the models and their scale can be quantified by considering the following relationship:

r = log10 (amplitude / resolution)

where the amplitude corresponds to the extent of the model - the range of the representation of reality it gives - and where the resolution gives the average separation between the points of the model. For example, the model of a street of a hundred metres with points separated, on average, by one centimetre gives an r value of 4. A topographical model of a hundred kilometres with an average separation of its points of 10 metres thus gives the same r value. A model of the whole Earth with a point separation of one centimetre can be associated with an r value of about 9.6. In comparison, the SRTM model with a point separation of about 30 metres leads to an r value of about 6.1, thus making it a purely topographic model, clearly neglecting details.

### Vector models 

- Ambigous in many ways
- Priviledge for territory representation

### Polygons models

- Polygon models can be seen as a specific "type" of vector model. Indeed, they can be defined as a set of surfaces defined by links between vertices, as in previous models. A purely polygonal model is thus a vector model with only triangles - allowing any type of surface to be constructed.
- Less used than vector modesl
- Used for 3D city models 

### Measures



### Format and Standards

PLY - Polygon File Format, paulbourke.net/dataformats/ply/

LAZ - format of LIDAR Data. (zLAZ proprietary version

3DS - 3D format

MNT - (Modele numerique de Terrain) : Elevation

DEM - idem 

ASC - Format of the SRTM -Shuttle Radar Topography Mission (SRTM),  a NASA mission conducted in 2000 to obtain elevation data for most of the world.



### Challenges

#### Size of models



### Visualizing 3D

### Game Engine Rendering



### Javascript Rendering

### OcTree

https://fr.wikipedia.org/wiki/Octree

Wikipedia : An **octree** is a [tree data structure](https://en.wikipedia.org/wiki/Tree_data_structure) in which each [internal node](https://en.wikipedia.org/wiki/Internal_node) has exactly eight [children](https://en.wikipedia.org/wiki/Child_node). Octrees are most often used to partition a [three-dimensional space](https://en.wikipedia.org/wiki/Three-dimensional_space) by [recursively subdividing](https://en.wikipedia.org/wiki/Recursive_subdivision) it into eight octants. Octrees are the three-dimensional analog of [quadtrees](https://en.wikipedia.org/wiki/Quadtree). The name is formed from *oct* + *tree*, but note that it is normally written "*octree*" with only one "t". Octrees are often used in [3D graphics](https://en.wikipedia.org/wiki/3D_graphics) and 3D [game engines](https://en.wikipedia.org/wiki/Game_engine).

The use of octrees for [3D computer graphics](https://en.wikipedia.org/wiki/3D_computer_graphics) was pioneered by Donald Meagher at [Rensselaer Polytechnic Institute](https://en.wikipedia.org/wiki/Rensselaer_Polytechnic_Institute), described in a 1980 report "Octree Encoding: A New Technique for the Representation, Manipulation and Display of Arbitrary 3-D Objects by Computer",[[1\]](https://en.wikipedia.org/wiki/Octree#cite_note-1) for which he holds a 1995 patent (with a 1984 [priority date](https://en.wikipedia.org/wiki/Priority_right)) "High-speed image generation of complex solid objects using octree encoding" [[2\]](https://en.wikipedia.org/wiki/Octree#cite_note-2)



Note from Bachelor thesis : 

Web technologies have several ways to display graphical content. Such content can either be internally generated from the web browser or received from a web server ready to be displayed.

For the first option where content is graphically rendered on the client’s machine on a browser, web technologies currently offer a limited amount of graphical rendering capabilities. Apart from static image files and Scalable Vector Graphics (SVG) files, HTML5 and JavaScript offer a Canvas onwhich programs can dynamically draw either with a simplified JavaScript API (Canvas API) or with a lower level graphical API: WebGL. Because of the very basic capacities of the former, we only will discuss about WebGL as an alternative to an OpenGL application. This option allows developers to draw images of 3D scenes in real time using a set of graphical commands to communicate with the machine’s Graphics Processing Unit (GPU). This type of solution is convenient to develop, as technologies in question are high level and fast to develop. This also relieves the developer of the application of having dedicated hardware to render the display, as it is the client machine’s task. The main drawback is that, as discussed in the next chapter, there are some performance losses due to layers of abstraction.

Plus : Simpliciity but 

Minus : no multithreading  not good perfomance because of Javascript 

The second option avoids needing the client to do the graphical computing, but instead needs a dedicated machine that plays the role of a rendering server. It periodically outputs images of the rendering process which can be exported and sent through the network to the front-end application on the web. This allows the developer to have control over the rendering power, as the quality and performance are responsibilities kept to the maintainer of the application and not to the end-user.

PLus : Works with simple device. 

GPU Revolution 

To maintain a scalable service of 3D rendering over the network, the maintainer can take advantage of cloud services that offer dedicated machines with high-end GPUs and take care of the hardware maintenance in case of failure or simply upgrades to newer materials. As the rendering engine is not limited toWebGL, the rendering engine could be developed with better optimized systems. Developing the engine at a lower-level means we can avoid data abstractions and some transfer flows during the process, to achieve better performance than Web. This of course have several drawbacks, the first being the cost of the service: there is another server to maintain online and which needs processing scalability on users demand. This is also a solution that demands more work put in the development of the application, needing knowledge in three different fields: low-level graphics programming, fast networking structures and web front-end application. In the time span of this project, a prototype was achieved that can be improved and completed in all three aspects.

Big question : Two scenarios : 

- Above the Web
- Under the web

### Mirror Worlds and 4D

Digital epiderm. 

The mirror-world will aim to be an up-to-date model of the world as it is, as it was and as it will be.

All objects (including representations of landscapes) of the mirror-world will be machine-readable, and, therefore, searchable, traceable and available to be part of simulations by powerful algorithms. In the mirror world, time will be a fourth dimension, as it will be very easy to go back to the past, at any location, reverting to a previous version kept in the log. One may also travel in the other direction, as future versions of a place can be artificially created based on all information available that can be used to anticipate a predictable future. Such “time-trips” will have an increased sense of reality, as they will be based on a fullscale representation of the present world.

Augmented Reality. 

## Practice

### How do conduct a photogrammetric campaign

### Using a Procedural software (e.g. Houdini)

### Using a Photogrammetric software (e.g. RealityCapture)

## Question and Answers 



