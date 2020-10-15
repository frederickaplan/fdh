---
title: 'Foundations in Digital Humanities 2.2'
subtitle: 'Document Structure'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Document Structure

## Theses

1) Describing the content of a document is a complex task

2) New open standards developed in the last 10 years offer a scalable approach to describe almost any kind of digital document 

3) Using the regulated representation approach, generic description of document information structure can be create and use for annotation and parsing

4) Using homologous pairs, underlying continuous fictional spaces can be modelled

## General structure of the pipeline

\> The World containing information-bearing objects and phenomena

(How is this information stored in the World)

\> Physical Document documenting this information 

(How is this information stored in the Physical document)

\> Digitised Document documenting the physical document 

(How is this information stored in Digital Document)

\> Standard Description of the structure of the document describing the structure of the physical document in a digital formalism

\> Extraction of content of the document 

\> Identification of content and link with other documents

\> Construction of World Models

## Content and Structure of a document

Digitisation produces ocean of images. The next steps are now to analyse their **content** , segment them in smaller units and link these units with one another. 

Two challenges

How can we describe the **structure** of a document ?

what is the **content** of a document ?

Some digitised documents are well structured at some level :

\- a book volume made a consecutive pages

Others have more complex structure

\- A box containing postcards

\- An “herbier” with pages not in a fixed order

\- A book with folded map inside

\- A book containing an inserted object 

We need a standard way to describe all these variety of ordered and unordered structures. 

Sometimes, the “content” of some object/pages is extremely complex to describe and articulate. 

In order to parse the content well, one need to understand precisely the way of circulating inside the document. 

Ideally we would like to find a way of unpacking the content of the object to bring back to smallest possible dimensions : dimension 0 (id of a referent), dimension 1 (text) , dimension (2) images or (in the worst case) dimension 3 or 4.

And connect these basic component first in a structured graph representing the document and then many in coherent fictional space. 

Describing the content is reducing the complexity of the object to smaller description. 

It is a kind of compression.

A compression is a fundamental form of understanding. 

## Circulations inside a document

Dimension 1 : A text is like a unidirectional path.Reading a text is like walking the path. (Reading fast is like running).

Dimension 2 : Pages are like closed surfaces with indicated entrances and exits and associated circulation rules.

Dimension 3 : A book is like a city, a 3D organization of closed spaces with complex circulation rules.

Sometimes the reader has no other choice than to move forward.

Branching : The reader can leave the main road to explore complementary circuits.

Sometimes, the reader can switch sideways.

Or get lost in a labyrinth. 

Annotation is a way to have content growing on top on existing content and complexify the structure even more. 

## Standards

Standards for describing content of document how greately improved in the last 10 years.

Now, a set of standards build on top of one another permits to solve the problem at planetary scale. 

### Open Annotation Model 

From a high-level perspective, the Open Annotation model is similar to many other related proposals (Annotation Graphs, DADA, LAF/GrAF, PAULA): 

•Annotations are standoff, that is, separate from annotated things, which are identified through references 

•Annotations form a graph where the annotations are nodes and can be referred to by other annotations 

•Annotations can associate data of arbitrary complexity with the thing being annotated 

Open Annotation Collaboration and Annotation Ontology Initiative jointly founded W3C Open Annotation Community Group to develop a common RDF-based specification for annotating digital resources.

The Open Annotation Core Data Model specifies an interoperable framework for creating associations between related resources, called annotations, using a methodology that conforms to the Architecture of the World Wide Web. 

An annotation is considered to be a set of connected resources, typically including a body and target, where the body is related to the target. 

•Annotation: a conceptual link between a body and a target 

•Body: a comment or resource which is ”about” the target 

•Target: the resource which is being discussed 

### Shared Canvas

Built upon Open Annotation, the Shared Canvas data model specifies a Linked Data based approach for describing digital facsimiles of physical objects in a collaborative fashion. It is intended for use in the cultural heritage domain, although may be useful in other areas. 

Instances of the data model are consumed by rendering platforms in order to understand the relationships between the constituent text, image, audio or other resources associated with an abstract Canvas, or parts thereof, via Open Annotations. 

A Canvas is an empty space in which to build up a display (Think a Powerpoint slide) 

•A SharedCanvas’s top left and bottom right corners correspond to the equivalent corners of a page (or a rectangular bounding box around it) 

Specific Resource with Selector to define an area of the Canvas 

•Text Selectors to describe the appropriate part of the text 

One canvas, multiple images. 

One image, multiple canvas.

### International Image Interoperability Framework (IIIF)

Every cultural heritage site tends be a silo, every digital archive is separated from the others. IIIF offers a global framework for organizing image storing and delivery at the worldwide scale. 

The International Image Interoperability Framework (IIIF) is driven by a group of research libraries, national libraries, and non-profit image repositories committed to opening access to cherished image resources 

•It encourages and supports the development of compatible image serving and viewing software that is easy to install and provides a good user experience 

•It is anchored by two well defined Link Data based APIs, compliant to the Shared Canvas Data Model: 

• IIIF Image API: pixel content via a simple REST web service
 • IIIF Presentation API: description to drive a remote viewing experience of a Cultural Heritage object 

320 M IIIF pages, and counting ..

A good point to start : 

https://github.com/IIIF/awesome-iiif

2011 : The Image API created as as a collaboration between The British Library, Stanford University, the Bodleian Libraries (Oxford University), the Bibliothèque nationale de France, Nasjonalbiblioteket (National Library of Norway), Los Alamos National Laboratory Research Library, and Cornell University.

2013: Presentation API

2016 : Search API

The [Universal IIIF Collection](https://graph.global/static/data/universes/iiif/universe.json)

Below are examples of IIIF manifests

| Description | Institution                                           | Catalog                                                      |
| :---------- | :---------------------------------------------------- | :----------------------------------------------------------- |
|             | Yale                                                  | http://manifests.ydc2.yale.edu/manifest                      |
|             | Stanford                                              | https://graph.global/static/data/universes/iiif/stanford.json |
|             | Biblissima                                            | https://graph.global/static/data/universes/iiif/biblissima.json and https://labs2.artstor.org/iiif/ssc/manifest.json |
|             | e-codices – Virtual Manuscript Library of Switzerland | https://graph.global/static/data/universes/iiif/e-codices.json |
|             | Sentences Commentary Text Archive                     | http://scta.info/iiif/collection/scta                        |
|             | Internet Archive                                      | http://iiif.archivelab.org/collection.json                   |
|             | TextGrid                                              | https://graph.global/static/data/universes/iiif/textgrid.json |
|             | ARTstor                                               | https://labs2.artstor.org/iiif/ssc/manifest.json             |
|             | Bodleian Library, Oxford                              | http://iiif.bodleian.ox.ac.uk/iiif/collection/All            |
|             | Wellcome Library                                      | http://wellcomelibrary.org/service/collections/              |
|             | Villanova University Digital Library                  | http://digital.library.villanova.edu/Collection/vudl:3/IIIF  |
|             | The Manuscriptorium                                   | [http://collectiones.manuscriptorium.com](http://collectiones.manuscriptorium.com/) |

## Synchronic Patterns and Diachronic Homology 

Some documents must be described in extension (the text of a novel). 

But other are highly regulated Cf. Course on Regulated Representations). 

We can extract and link the information in a more efficient way. 

Two challenges

Synchronic : How can extract the information which is in regulated representation in a structured way from the same family of synchronic regulated representations. 

Diachronic : How can we link content from different regulated representations and identify it as being the same. 

### Synchronic - information schema

A regulated representation can be associated with a specific information schema, that can be fully described in XML or JSON.

This schema permits to automatically generate an annotation interface.

### Diachronic - homologous pairs

To identify two mentions as referring to the same referent is a process of homology. 

This is something fundamental that we will see again and again in this course. 

The correspondance of homologous points define “pivot” points. Pivot points are the invariants features, the "sameness" that is characterised by the homologous pairs. 

We can also say that they define a equivalence class. 

We can define the coordinate of a pivot point or a unique reference ?

But do the “pivot” points exist ?

The more a pivot point is articulated, linked with documents “views” and with other pivot points, the more it is real/coherent. 

The stronger the correspondant fictional space. 

Until recently, the only way to identify homologous points was to establish manual process of identifying them.

Now algorithm can recognise some homologous points automatically and thus create more pivot points and a denser and more articulated representation of fictional spaces. 

This imply that our representations of reality are likely to change drastically in the next 20 years. 

## Summary

Describing the content of a document is a complex challenge 

Some international standards help doing so (Open Annotation, IIIF)

Structured information can be annotated and extracted out of Regulated Representations 

Homologous pairs permits to create an underlying continuous fictional spaces. 

## In the next course

Next, we will start to go into details for each categories of documents. 

## Further reading

- Paul Otlet, Le livre sur le livre
- Salaum, Arsenault, Introduction aux sciences de l'information. 
- Anthony Grafton, La page de l'Antiquiét à l'ère du numérique : Louvre editions 
- 