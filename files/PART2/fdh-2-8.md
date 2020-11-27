---
title: 'Foundations in Digital Humanities 2.8'
subtitle: 'Image Processing'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Image Processing

## Theses

1) State of the art image analysis permits to extract metadata out of artwork photographs

2) … and compute similarities between images



## Example of an image pipeline

### Digitisation

Digitisation images in context... some important point to take into account. 

### Segmentation

dh-segment: Generic framework for segmentation

Practicula use case : 

Annotations can be done with online or offline tools : 

- cvat.org (also with IIIF)
- Gimp

5 golden rules for annotation (from Remi Petitpierre)

1. A class should bbe concretely embodied
2. A class should share common figureative, topological and morphological codes. Background can be used for anything else
3. Reduce the number of classes of a minimum
4. Think like a machine. Apply the same reasoning each time.
5. Start small and test. Youenver know how many annotations will be nedded. 

### Metadata extraction

Metadata is data about data sometimes present "around" the images (on a cardboard for instance)

### Link with reference database

### Detection of physical connection

Detection of duplicates. 

### Detection of non-coherent metadata

Some images that were thought to represent the same object represents different paintings.

Vice versa, the same painting may have conflicting metadata. 

## Vector description

Story of the Imagenet competition 

- 100 000 concepts (WordNet)
- 1000 images per concepts

Vector description are obtained as hidden layers of neural networks trained for classication tasks. 

Similarity between two images as Inner product of vector descriptions

## Metric Learning

Metric learning permits to learn new invariants specific to painting similarities, learning for instance to ignore textural features. 

(Ai - Bi) > (Ai - Ci)

S (Ai, Bi) > S (Ai, Ci) in R. (Local consistencies)

S (Ai, Bi) - S (Ai, Ci) > 0

Hinge loss function

## Searching in collections

IIIF coding

Mixing text and image in queries

Algebraic queries (Combining several images in positive and negative)

2D maps

## Summary 

Image analysis pipeline permit to construct the morphograph in a semi-automatic manner and recognize incoherent attributions 

## In the next chapter

Like for text, the next chapter concern knows knowledge extraction out of images. 

## Further reading

- Seguin, B. Striolo, C., di Lenardo, I. and Kaplan. F. (2016) Visual Link Retrieval in a Database of Paintings, VISART Workshop, ECCV, Amsterdam, September, 2016

