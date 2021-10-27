---
title: 'Foundations in Digital Humanities 2.7'
subtitle: 'Image systems'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Image systems

<!--This chapter needs to be rewritten on the basis a taxonomy of 4 image systems.see  I sistemi di immagini nell’archivio digitale di Vico Magistretti. Please wait before improving it--> 

<!--Part of the new concepts have been reintroduced but the entire strucure needs to be rethought.--> 

<!--For coherence, part of this classification could also be introduced for texts.--> 



## Theses

1. Images like texts can be represented as systems

2. At least 4 image systems can be identified. 

## Definitions

### Image systems

We have seen what a Writing System is. What are Image systems?

> Definition : An Image system is a graph of connected digital images and a set of rules for deciding when two images are linked. 

A digital archive is most likely organized following numerous systems of images, which often overlap and intertwine, but once formally identified, allow an organized exploration and analysis of the whole set of graphic documents. These systems could reveal the centrality of some image-documents, the existence of coherent sub-sets in the corpus, or links and connections not always known. 

### Type 1: Conceptual-based image systems

> Definition : a system of images on a conceptual basis links images that can be described by common concepts. 

In this network, two images are linked if they can be characterized by a common conceptual descriptor. It can be for example the same category of objects (table, chair, lamp or building). 

Conceptual-based image systems are naturally hierarchical, some concepts are by nature more general than others. A large database like ImageNet associates to each word several thousand images of examples. 

This hierarchical image system has played a crucial role in the development of new machine vision techniques in the years 2010 that show the superiority of deep learning approaches. Today it is in fact possible, for a computer, to recognize without difficulty thousands of conceptual categories. For an image archive, this system allow to perform simply an automatic categorization of images by associating to each of the conceptual 'tags'. On the basis of this categorization an interface can be developed that allows you to navigate the resulting image map navigating from image to image that have common concepts and following their proximity. 

In Art History various concept-based ontology are used. One of the most recent one is Iconclass, organised in 3 levels of abstractions. 

More generally, the work of Aby Warburg was dedicated to the definition of large-scale ontology to classifiy hierachically images. His work is continued by the Warburg Institute. 

### Type 2: Image systems based on named entities

> Definition: an image system based on named entities binds images representing the same named entities. 

A named entity is an entity uniquely and unambiguously identified by a name. It can be a person, an object, even a serial product, or a specific building.

The co-presence of the same named entity in two different images represents a stronger link than the conceptual one. This image system is therefore often a subset of the previous one. 

The image system can be articulated through references in international databases such as Wikidata. In fact, in Wikidata each named entity is associated to a specific number.

In this way it is possible to trigger a dual process, i.e. to effectively complete the information present in the archive by benefiting from the data produced by other international organizations and in turn integrate the international databases with the information extracted from the archive

### Type 3: Image systems based on perspective connections

> Definition: An image system based on perspective connections binds images for which it is possible to establish that they visually document the same reality from different perspectives.

This type of image system is often a subset of the second type of images (based on named entities). However, the constraint here is stronger. The perspective angles of two images must overlap in order to converge on the same reality. It is a matter of identifying pairs of homologous points in the two digital images. 

It can be, for example, two photographs captured from two different angles, but very close to each other. Instead, a frontal photo of a building will not have points in common with a photo representing the opposite side. These two photos will be connected rather by a system based on named entities but not by a system based on perspective connection. 
When two images are visually linked it is in fact possible to automatically find a significant number of pairs of homologous points organized according to a precise geometry. Moreover, a photogrammetric calculation based on these homologous points allows to produce a partial 3D model of the represented object. In general, this configuration of homologous points is like a digital signature of the object, a distinguishing feature that allows it to be found in other images in the archive, and also in the 'net'. 

### Type 4: Image systems based on morphological relationships

> Definition: a system of images based on morphological relationships relates images for which it is possible to visually establish that they have a specific morphological motif in common and that one is the source of the other in a sequence of transformations or that they share a common morphological image-source.

For example, it is necessary to establish relationships between a preparatory sketch  and the final product. When a form is born, and is represented, it embodies a morphological motif that is specific enough to show that its presence in a subsequent document cannot be the result of an accidental reinvention. The system formalizes the trace of the morphological transmission sequences from the preparatory sketch to the technical drawing, from the prototype to the finished product, documenting, in short, the life of a form. 

It is only recently that computerized vision techniques (computer vision) have been able to obtain satisfactory performances for this type of analysis, offering for the first time an operationalization of the concept of morphological relationship. One of the main difficulties is represented by the need to detect the invariance of the form in a set of documents characterized by extremely diverse materiality and textures: pencil drawings, black and white or color photographs, technical models, among others. 
Based on examples of morphological connections, it is necessary to deform the visual space of the computer to find the morphological connections within the countless differences that characterize these images. 

These morphological sequences are creating a relationship of forms between the images and establishing, connection after connection, an immense morphograph in which the links that cross geographies and cultures are woven.  

## Homologous pairs and Physical closure

<!--To be rewritten not using the term Physical but writting about perspectives -->

We have seen what homologous pairs are. Images can be articulated with one another if they overlap the same physical reality. This reality is made of pivot points. 

> Definition: Homologous points are corresponding pairs of points in two digital images identified as the representation of the same underlying physical point, called pivot point, from two perspectives.

Can homologous points work with paintings ?

Strict homology works only if there is a physical connection between the image. They are overlapping representation of the same real object/place. 

> Definition : The connection between two digital images is said to be physical if it is possible to assert, from the visual information only, that they have an overlap covering the same physicality

Given a collection C , and A ∈ C ,B ∈ C , the connection (A–B) s

Ex : 

- A is a close-up of B
- A and B are engravings coming from the same wood-block

> Definition: The physical closure of an image is the set of images for which there is path of physical connection leading to this image, the image system defined by the physical connection rule.

Given a collection C , the physical closure of an image A ∈ C is the set of images for which there is path of physical connection leading to A.

## Dimensions of similarity

### Content / Subject / Topic

Images can be related in terms opf content, subject or topic

### Morphological Patterns

Images are linked through visual connections i.e. morphological patterns. 

Pattern propagation is similar to Text Reuse

- Reconstruction of a “Philology” of images, like the tree and systems of texts. 
- Identification of the Image 0. 

Complex transmission network : Images can be linked through complex compositions of patterns. 

There is an autonomy of the subject and an autonomy of the shape. They circulate independently.

The same morphological pattern can be used in different subjects. 

Example : The arm of Leda. 

### Style and Texture

Texture is a third dimension, not clearly identified as an independant factors in Deep learning research. 

## Metrics and ordering

Agreement (intersection) of partial orderings are partial orderings. 

Collective creation of a *Morphograph* (𝓓)

For the morphograph to be largely consistent it is important that 𝜔p → 𝜔(𝓓), the knowledge of any person should tend to the knowledge of everyone.  

A search engine can be built using deep learning network trained on a partial Morphograph. 

This search engine helps building a finer and wider Morphograph. 

## Summary 

Various forms of connections exist between images, from the overlapping of the same “reality” to an organised order of morphological similarity. 

## In the next chapter

We will explore how the image processing pipeline can compute automatically large image networks and morphographs. 

## Further reading

- Benoit Seguin's PhD. Thesis : Making large art historical photo archives searchable
- Scott McCloud, Understanding Comics
- Kaplan, F. and di Lenardo, I sistemi di immagini nell’archivio digitale di Vico Magistretti 

