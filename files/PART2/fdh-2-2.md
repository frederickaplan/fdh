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

# FDH-2-2: Document Structure

#### Theses

1) Describing the content of a document is a complex task

2) New open standards developed in the last 10 years offer a scalable approach to describe almost any kind of digital document

3) Using the regulated representation approach, generic description of document information structure can be create and use for annotation and parsing

4) Using homologous pairs, underlying continuous fictional spaces can be modelled

#### Contents
> 1. General structure of the pipeline
> 2. Content and structure of a document
>> 2.1. Describing the structure // 2.2. Modelling the content // 2.3. Types of circulations inside a textual document //
> 3. Standards
>> 3.1. Open Annotation Model // 3.2. Shared Canvas // 3.3. International Image Interoperability Framework (IIIF) //
> 4. Synchronic patterns and Diachronic homology
>> 4.1. Synchronic: Information schema // 4.2. Diachronic: Homologous pairs //
> 5. Conclusion
>> 5.1. Summary // 5.2. In the next chapter //
---
## 1. General structure of the pipeline

1. **The World**, containing information-bearing objects and phenomena (How is this information stored in the World?)
2. **Physical document**, documenting this information (How is this information stored in the physical document?)
        3. **Digitised document**, documenting the physical document (How is this information stored in digital document?)
    4. **Standard description of the structure** of the document describing the structure of the physical document in a digital formalism
            
        5. **Extraction of the content** of the document
            
            6. **Identification of the content** and link with other documents
            
                7. **Construction of World Models**

---
## 2. Content and structure of a document

Digitisation produces oceans of images. The next steps are now to:
- analyse their **content**,
- segment them in smaller units,
- and link these units with one another.

Along any digitised object will come two challenges:
1. How can we describe the **structure** of the document ?
2. What is the **content** of the document ?

### 2.1. Describing the structure

Some digitised documents are well structured at some level. For example, a book volume will (nicely) yield consecutive pages.

However, others have more complex structures, and can contain several objects: a box containing postcards, a book with folded maps inside, an herbarium with pages not in a fixed order, a book containing an inserted object — all of these objects raise the question of **whether its structure has an intrinsic value**.

This is why we need a standard way to describe all these varieties of ordered and unordered structures.

### 2.2. Modelling the content

Sometimes, the “content” of some object/pages is extremely complex to describe and articulate.

In order to parse the content well, one need to understand precisely the way of **circulating inside the document**.

Ideally we would like to find a way of unpacking the content of the object to **bring back to smallest possible dimensions**: dimension 0 (ID of a referent), dimension 1 (text), dimension (2) images, or (in the worst case) dimension 3 or 4.

We can then try to connect these basic components: first in a structured graph representing the document, and then by regrouping many of them into a coherent fictional space.

The added value of describing content lies in the ability to reduce the complexity of the object to smaller description. It is a kind of compression. And **compression is a fundamental form of understanding**: the higher the compression, the better the understanding.

### 2.3. Types of circulations inside a textual document

- **Dimension 1**: A text is like a unidirectional path. Reading a text is like walking a path. (Reading fast is like running).

- **Dimension 2**: Pages are like closed surfaces with indicated entrances and exits, and associated circulation rules (hyphen, page break, footnotes, content boxes, etc.)

- **Dimension 3**: A book is like a city, a 3D organization of closed spaces with complex circulation rules.

Sometimes the reader has no other choice than to move forward. But at branching events (footnotes, captions, ...), the reader is faced with a decision. He can leave the main road to explore complementary circuits.

Annotation is a way to have content growing on top on existing content and complexify the structure even more.

But behind all "additional" content, grown on top of the original structure, lies the question of what to do with it: should it be digitised? If so, how? _Answering this question was the motivating factor in the introduction of standards._

---
## 3. Standards

Standards for describing content of document have greatly improved in the last 10 years.

Now, a set of standards build on top of one another permits to solve the problem at a planetary scale.

### 3.1. Open Annotation Model

From a high-level perspective, the **Open Annotation Model** is similar to many other related proposals (Annotation Graphs, DADA, LAF/GrAF, PAULA), in that it considers annotations as **standalone content**:

- Annotations are standoff, that is, **separate** from annotated things, which are identified through references.

- Annotations form a **graph** where the annotations are nodes and can be referred to by other annotations.

- Annotations can **associate** data of arbitrary complexity with the thing being annotated.

Open Annotation Collaboration and Annotation Ontology Initiative jointly founded the W3C Open Annotation Community Group to develop a common RDF-based specification for annotating digital resources.

The Open Annotation Core Data Model specifies an interoperable framework for creating associations between related resources, called annotations, using a methodology that conforms to the Architecture of the World Wide Web.

An annotation is considered to be a **set of connected resources**, typically including **a body and target**, where the body is related to the target. In this basic data model, the elements of the documentation are:
- **Annotation**: a conceptual link between a body and a target. To this "annotation", a lot of details can be attached: its ID, author, motivation, etc.
- **Body**: a comment or resource which is ”about” the target
- **Target**: the resource which is being discussed

### 3.2. Shared Canvas

Built upon Open Annotation, the Shared Canvas data model specifies a Linked Data based approach for describing digital facsimiles of physical objects in a collaborative fashion. It is intended for use in the cultural heritage domain, although it may be useful in other areas.

Instances of the data model are consumed by rendering platforms in order to understand the relationships between the constituent text, image, audio or other resources associated with an abstract Canvas, or parts thereof, via Open Annotations.

A **Canvas** is the empty 2D space on which to build up a display (it can be thought of as a Powerpoint slide).

A Shared Canvas’s top left and bottom right corners may correspond to the equivalent corners of a page (or a rectangular bounding box around it). On top of that are added many layers of different boxes of Commentary, Transcriptions, Annotations, etc. — to which are associated Text Selectors describing the appropriate part of the text.

Both "One canvas - Multiple Images" or "One image-Multiple canvases" (eg. to document the same image in a different manner) are valid configurations.

Overall, the Canvas object and the versatility it provides may very much be the solution to the problem of **standardly storing of any form of digitised information**.

_Using both of these ideas (Open Annotation and Shared Canvas), a new standard has emerged and has since been widely accepted: the IIIF standard._

### 3.3. International Image Interoperability Framework (IIIF)

#### 3.3.1. Presentation of IIIF
Every cultural heritage site tends be a silo, every digital archive is separated from the others, with little to no room for a common usage of the digitised image. The **International Image Interoperability Framework (IIIF)** stemmed from this frustration and was born from the common efforts of academic figures. IIIF offers a global framework for organizing image storing and delivery at the worldwide scale.

The International Image Interoperability Framework (IIIF) is driven by a group of research libraries, national libraries, and non-profit image repositories committed to opening access to cherished image resources.

It encourages and supports the development of compatible image serving and viewing software that is easy to install and provides a good user experience

It is built on two well defined Link Data based APIs, both compliant to the Shared Canvas data model:

1. **IIIF Image API**, which is responsible for delivering the image (pixel) content via a simple REST web service.

2. **IIIF Presentation API**, a way to organise a collection, in a readable and understandable manner, (ie. a remote viewing experience of a Cultural Heritage object).

As of 2020, more than 320M pages follow the IIIF standard, and counting ...  A good place to start is: https://github.com/IIIF/awesome-iiif

IIIF started in 2011, with the creation of the Image API, started as as a collaboration between The British Library, Stanford University, the Bodleian Libraries (Oxford University), the Bibliothèque nationale de France, Nasjonalbiblioteket (National Library of Norway), Los Alamos National Laboratory Research Library, and Cornell University. The Presentation and Search APIs were respectively presented in 2013 and 2016.

Some examples of IIIF manifests include:
- [Yale](http://manifests.ydc2.yale.edu/manifest)
- [Stanford](https://graph.global/static/data/universes/iiif/stanford.json)
- [e-codices – Virtual Manuscript Library of Switzerland](https://graph.global/static/data/universes/iiif/e-codices.json)
- [Internet Archive](http://iiif.archivelab.org/collection.json)
- [Bodleian Library, Oxford](http://iiif.bodleian.ox.ac.uk/iiif/collection/All)

#### 3.3.2. Working of IIIF
(_Throughout this subsection, capitalised names refer to classes from the IIIF Manifest API._)

Firstly, instead of considering an image as a static file, the IIIF standard prefers a **client-server relation**, through which the image can be simply delivered, before being modified if needed (truncated, recoloured, rescaled, etc.); and that without the need to download the original image first nor affecting it.

Then comes a more powerful idea: the existence of a so-called **Manifest**, which is the overall description of the structure and properties of the digital representation of an object. The Manifest scale is the unit of digitisation (a book which contains pages, a box which contains postcards, etc).

The list of objects and collections is described by the **Collection**. The Manifest is effectively a series of Canvases (cf. 4.2.), on top of which are stored images, texts, and annotations (Content and Anno).

As IIIF was built with open-access and collaboration in mind, it is **notably easy to "ingest" other collections**: for that, only a "top-node" URL is required (pointing to the desired Collection or Manifest).

---
## 4. Synchronic patterns and Diachronic homology

While some documents cannot but be described in extension (the text of a novel), others which are **highly regulated** (cf. FDH-1-3) **can have their information extracted in a more efficient way**.

This potential pattern recognition can take two forms:
1. **Synchronic**: How can extract the information which is in regulated representation in a structured way from the same family of synchronic regulated representations.

2. **Diachronic**: How can we link content from different regulated representations and identify it as being the same.

### 4.1. Synchronic: Information schema

A regulated representation can be associated with a specific information schema, that can be fully described in XML or JSON.

This schema permits to automatically generate an annotation interface.

### 4.2. Diachronic: Homologous pairs

To identify two mentions as referring to the same referent is a process of homology. This is something fundamental that we will see again and again in this course.

> Definition: Homologous points are corresponding pairs of points in two digital images identified as the representation of the same underlying physical point, called pivot point, from two perspectives.

or more generally 

> Definition: Homologous points are corresponding pairs of points in two digital documents identified as the representation of the same underlying reality, called pivot point, from two perspectives.

The same city marked with points of two maps, same person identified at several places in a text, the same building corners viewed from different angles are exmaples of homologous pairs. 

The correspondence of homologous points define **“pivot” points**. Pivot points are the **invariants features**, the "sameness" that is characterised by the homologous pairs. We can also say that they define an equivalence class.

The coordinates of a pivot point and a unique reference can be defined. **_But do the “pivot” points exist?_**

Pivot points do come from multiple reference, with precise spatial positions; yet, they are never directly observable, only through the documents. Temporally, pivot points stand for a **"continuous reality"** between the different times at which the documents were captured.

The more a pivot point is articulated, linked with documents “views” and with other pivot points, the more real and coherent it is, and the **stronger the correspondent fictional space**. The validity of pivot points are assessed by the diachronic and geometric comparaison with other reference points.

**Identifying homologous pairs**

Until recently, the only way to recognise homologous points was to establish manual processes to identify them.

Now, **algorithms can recognise some homologous points** automatically and thus create more pivot points and a denser and more articulated representation of fictional spaces.

This imply that our representations of reality (and its past) are likely to change drastically in the next 20 years.

---
## 5. Conclusion
### 5.1. Summary

- Describing the content of a document is a complex challenge.

- Some **international standards** help doing so (Open Annotation, IIIF).

- Structured information can be annotated and extracted out of Regulated Representations.

- Homologous pairs permit to create an underlying **continuous fictional space**.

## 5.2. In the next chapter

Next, we will start to go into details for each category of documents.

## Further reading

- Paul Otlet, Le livre sur le livre
- Salaum, Arsenault, Introduction aux sciences de l'information.
- Anthony Grafton, La page de l'Antiquiét à l'ère du numérique : Louvre editions

## To improve

- Should the part on homology be treated here or transfer later on with the discussion on image systems (FDH 2-7)
- Should introduce Otlet's ontology of documents as discussed in "Traité de documentation : Le livre sur le livre". A well-formed document ontology is a basic foundation for Digital Humanities. 

- Should this part be organised in like the others : Document Systems, document processing, Documenting Understanding ...
- The footnote could be developed as an example (cf Grafton)