---
title: 'Foundations in Digital Humanities 3.0'
subtitle: 'Introduction to part 3'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document


---

# Introduction to Part 3

## Rearticulation of the concepts introduced so far

### Information

> Definition:  Information is a difference that makes a difference for an interpreter

This means that information is latent, waiting to be revealed, interpreted, translated. 

It is always defined based on an interpretation process. 

### Memory

> Definition: A memory is a a set of stored information

Any shape is a memory storage.Memory is stored in asymmetries and erased by symmetries. Building, living beings, rocks are memory stores. 

### Glyph

> Definition : A glyph is a memory storage unit taking the form of visually distinguishable shape.

It can be read as a character (or a group of characters)  of a writing system. This is one form of translation. 

Once this translation is done, its geometrical nature is lost. It has become an abstract symbol. 

### Script and characters

> Definition: A script is a set of conventional symbols called characters or grapheme that can be used to represent in writing, one or more languages. ¨

### Writing systems

> Definition: A writing system is the use of a script in a particular language. The writing systems defines rules and convention on how to interpret the scripts and which sequences of characters are allowed or not. 

Writing systems exist for natural language (English, French) but also for programming languages, computation systems, etc. 

A ancient goal of the humanity is to define a universal writing system capable of describing everything

-  Magic Languages of John Dee
- Raymond Lull’s Ars Magna
- Yi King
- Leibniz’s lingua generalis and convention for calculus
- Pierre Levy's semantic sphere
- Wolfram Language

Writing systems can also be used to describe shapes. 

As we saw, the shape of curve can be documented using sequences for deformation operations (Leyton’s Generative theory of share and Process Grammar)

The shape of a glyphs can be conventional encode/redocumented/rewritten in a standard character chain (UNICODE)

### Digital images systems

In some sense, a digital image is part of particular writing systems based on operation to manipulate and transform arrays. 

> Definition : A digital image is a raster or two-dimensional array of points. Each point, or pixel, is defined by unique integer coordinates. 

Computational operations on digital images are a powerful language. 

We saw that digital images can be articulated with one another. 

> Definition : An Image system is a graph of connected digital images and a set of rules for deciding when two images are linked. 

### Image systems based on physical connections

A particular image system is the one defined by the concept of physical connection. 

> Definition : The connection between two digital images is said to be physical if it is possible to assert, from the visual information only, that they have an overlap covering the same physicality

The same physicality is defined here as viewing the the same object or being the output of the same serial production.

The signature of such a physical connection can be computed algorithmically based on strong geometrical invariants shared by the two images. 

> Definition: The physical closure of an image is the set of images for which there is path of physical connection leading to this image, the image system defined by the physical connection rule.

If there is a physical connection between two digital images (if they are part of the same image system based on physical connection), several homologous points can be defined. 

> Definition: Homologous points are corresponding pairs of points in two digital images identified as the representation of the same underlying physical point, called pivot point, from two perspectives.

Each points in an image have 2D integer coordinate (relative to the image height and width).
Using geometrical calculus (photogrammetry) it is possible to associated to the pivot a point a series of approximate 3D coordinate in a corresponding relative 3D space.

If the images are georectified, the 3D space can be articulated  relatively to the surface of the Earth. 
The pivot point (3D coordinate) and the homologous pairs (2D coordinate) is thought to represent the same continuous physical reality. 

Symmetrically, the presence of numerous coherently organised pairs of homologous points is the signature of physical connection, an underlying common physical reality. 

### Image systems based on morphological connections

We saw also that some images with no physical connection could be linked if they shared morphological patterns. This is another kind of image systems, superimposed to the one based on physical connection. 

The morphological patterns is thought to be transmitted from one image to the other through an imperfect copy process. This meant that a part of one image was the source playing a role in historical operation that lead to the creation of the other image (copy in workshop). 

The morphological link is the sign of some sort of casual relation between the images. 

> Definition : The connection between two digital images is said to be morphological if it is possible to assert, from the visual information only, that one was at some point the source of the other in a chain of copies. 

The presence of morphological link permits to establish a partial ordering on the digital images. 

A search engine was built following this principle, permitting an augmentation of the scholar’s search space and helping establish the causal dependency tree and progress in the approximation of the causal chains.

### Map systems

We studied maps and map systems.

> Definition : Maps systems articulate digital images with geometrical approximations of places. 

A place can be defined in the following way 

> Definition : A place is a non-ambiguous symbolic area where events can happen and typically defined in relation with other small or bigger areas. 

Every place has a concrete shape 

> Definition: A concrete shape of a Place is the actual and precise frontier of the place on the territory at a given moment in time. A place is characterised by a sequence of concrete shapes. 

Concrete shapes are linked with geometries. 

> Definition: A geometry of a concrete shape is an documented approximation

Geometries can be approximation on maps, measurement on the terrains. 

Geometries are typically defined as logical combination of polygons in relation to another surface. 

Some of the control points of these polygons are have homologous in other document and can therefore be associated with pivot points with 3D coordinate. We can talk about homologous geometries. 

### 3D Shapes

3D shapes can be approximated in three complementary ways

\- by sets of cloud points (3D) with corresponding homologous pairs

\- by projection of 2D geometries (some of which based on control points)

\- by sequence of process transformation as part of formal writing systems describing shapes in a procedural manner. 

3D shapes can play the role of pivotal structures for articulating the content of these different writing systems.  

### 4D indexes

We have described a way of indexing 4D spaces with a fully order index based on a system of division of cubes, permitting to define equivalence classes at various scales. This 4D index can be georectified to fit the surface of Earth. 

This 4D index is complementary to many of other indexes we encountered. 

### Points and vectors 

More generally, points can be 

\- 2D pixel on a digital image, control points of a curve

\- 3D (Pivot) points

\- Complex entities in (more or less high dimension) embeddings : Paintings in shape space, Words in large word space, Discourse in discourse space

Vectors 

\- Can link geometric (2D or 3D) points, words, paintings, discourses

\- Can be organised in polylines, polygons and arbitrarily complexe shapes in n-dimensional spaces. 

\- Can be used for evaluating similarity by calculating vectorial products. 



## Processing everything in a single computational system

### Open challenges

Can we process all these various kinds of extracted information in a single computational system ?

A challenge much like the Leibnizian's dream of *Lingua Generalis* 

Can we define ways for detecting facts from fictions ? Or criteria for reconstructing what really happened ?

### Irreductibility Principle

In this part of the course we will follow Bruno Latour’s Irreductibility Principle (Latour)

*Nothing can be reduced to nothing*

The different symbols and measures we are extracting are linked with one another through various forms of translations (some mathematical and some not). 

None of them can be reduced to another one. 

### Actor-Network Approach 

Points, Geometries, Documents are all actors. 

Each actors is connected to other in a network of relationship. 

Nothing exist outside these relationships. 

### Punctualisation

Most of the entities we have seen are complex systems (form a single page of a document to the description of a building). Sometimes, some actors stands for others, hiding the inherent complexity. 

This effect is know as punctualisation. 

> Definition : Punctualisation is the translation process of representing a complex system with a single point standing for this complexity

It is similar idea that the idea of encapsulation in object-oriented programming. 

The punctualisation process creates a black box that may not need to be open. 

### History recovery problem

Everything is flat. There is no hierarchy. Zombies, atoms and carrots have an equal dignity in this modelling approach.  Only actors and relationships. Only points and vectors. 

But each shape, person, thing is an history, a memory store.Each shape, person, thing is a point/black box that can be unpacked, de-punctualised.   

Can we unpack any encapsulated point into a sequence of events ? Can the whole world become a unique giant sequence of events ?

> Definition : The History Recovery Problem is the recursive challenge that consist in systematically expanding each entity into a sequence of finer grained events.

This is the subject of this part of the course. 



## Further Reading

- Schaeffer, Tresch, Gagliardi, Aesthetics of Universal Language

- Levy, la sphere semantique

- Stephen Wolfram, An elementary introduction to the Wolfram Language

- Latour, B., 2005. *[Reassembling the Social: An Introduction to Actor-Network-Theory](https://en.wikipedia.org/wiki/Bruno_Latour#Reassembling_the_Social)*. Oxford: Oxford UP

- Graham Harman, Object Oriented Ontology : A new theory about Everything

- Akrich, M., M. Callon, B. Latour, 2006, Sociologie de la traduction. Textes fondateurs, Paris, Les Presses des Mines

- Information

  

  