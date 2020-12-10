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

# FDH-2-8: Image Processing

#### Theses

1) State of the art image analysis permits to extract metadata out of artwork photographs

2) … and compute similarities between images

#### Contents
<!-- TOC depthFrom:1 depthTo:4 withLinks:1 updateOnSave:0 orderedList:0 -->
- [1. Example of an image pipeline: the Cini collection](#1-example-of-an-image-pipeline-the-cini-collection)
	- [1.1. Digitisation](#11-digitisation)
	- [1.2. Segmentation](#12-segmentation)
	- [1.3. Metadata extraction](#13-metadata-extraction)
	- [1.4. Link with reference database](#14-link-with-reference-database)
	- [1.5. Detection of physical connection](#15-detection-of-physical-connection)
	- [1.6. Detection of non-coherent metadata](#16-detection-of-non-coherent-metadata)
- [2. Vector description: Convolutional Neural Networks](#2-vector-description-convolutional-neural-networks)
- [3. Metric Learning](#3-metric-learning)
- [4. Searching in collections: the Replica engine](#4-searching-in-collections-the-replica-engine)
- [5. Conclusion](#5-conclusion)
	- [5.1. Summary](#51-summary)
	- [5.2. In the next chapter](#52-in-the-next-chapter)
- [Further reading](#further-reading)

<!-- /TOC -->


## 1. Example of an image pipeline: the Cini collection
In his PhD work, Benoit Seguin attempted to computationally detect similarities between paintings digitised from the physical collection of cardboard reproductions at the Cini foundation.

We will now describe the different steps in the processing of that image collection.

### 1.1. Digitisation
It starts with the digitisation of hundreds of thousands of images, all stored as photographs on some cardboards, with some associated metadata (typeset or handwritten).

### 1.2. Segmentation

A neural network then attempts to separate the image from the metadata by segregating the digitised cardboard into two regions. The developed network, ***dh_segment***, has been designed as a generic framework for segmentation, and can thus be used to tackle a great deal of problems, with the help of appropriate annotations. Examples of such problems include for example the detection of ornaments or illustrations in historical documents, the extraction of geometries from maps, the untangling of different layers of texts (commentaries vs. core content in medieval manuscripts), etc.

The annotations the networks uses to train itself can be simply be thought of as a series of masks, onto which different semantic classes are identified (usually by producing a multi-coloured raster image). The 5 golden rules for annotation are (from Remi Petitpierre) :
1. A class should be **concretely embodied**.
2. A class should share **common figurative, topological, and morphological codes**. A background class can be used for anything else.
3. The number of classes should be **kept to a minimum**.
4. **Think like a machine**. Apply the same reasoning each time.
5. **Start small and test**. One never knows how many annotations will be needed.

Note : Some recent techniques permits to envision self-configuring methods for segmentation (cf. nnU-Net: a self-configuring method for deep learning-based biomedical image segmentation).

### 1.3. Metadata extraction
Now that the region containing the metadata (ie. the "data about the data") has been identified and isolated, comes the questionsue of extracting its information. There are two problems to be tackled: the recognition of typographic characters (Optical Character Recognition), and the grouping of characters first into words and then into metadata fields.

### 1.4. Link with reference database
As of today, about 97% of metadata is recalled, 73.8% of which can then be disambiguated by being matched to an artist entry from the Getty Union List of Artist Names (ULAN Database).

There however exists entries for which the authorship is not always established; either because the work is anonymous, or is said to come from a workshop (such can be the case when the artwork indeed comes from a specific workshop, or in other cases simply when the work bears some resemblance to an artist's style).

### 1.5. Detection of physical connection
More interestingly, duplicates can be detected; this used to be simply unthinkable before the creation of algorithmic methods (manual comparaison is not possible at such scales, for hundreds of thousands of images). 88,000 images were found to be part of a duplicate group, which accounted for 34,000 objects.

### 1.6. Detection of non-coherent metadata
Out of these duplicate objects, about 1,340 (ie. 7%) have conflicting metadata. Some images that were thought to represent the same object represents different paintings. Vice versa, the same painting may have conflicting metadata.

## 2. Vector description: Convolutional Neural Networks

Computer vision has experienced a boom in the recent years, thanks notably to the (now well-known) ImageNet competition, in which a word is to be associated to an input image. The ImageNet database consists of 14 million images, with a word (taken from the 100,000 concepts WordNet database) associated to each.

Following the introduction of Convolutional Neural Networks, the error rate of the best ImageNet competitors suddenly dropped from around 35% in 2012 to less than 8% three years later. When using CNNs, the input image is decomposed (layer after layer) into smaller and smaller, as well as more abstract, images -- the idea being that, after a sufficient number of abstractions, the classification becomes straightforward enough.

By reusing the hidden layers of a network pre-trained for classification tasks, fixed-length vector descriptors can be obtained. This becomes a very powerful tool: ***the similarity between two images is then simply the inner product of their vector descriptions***.

Once our CNN model is trained to classify the 500,000 images digitised from the Cini database, we can get the images' vector descriptions and (relatively straightforwardly) cluster them such that their morphological _and_ figurative similarity becomes visually obvious. This is already a very valuable and impressive result. But how do we go further? By transforming the space of these descriptive vectors such as to follow the learning of similarity between paintings. This is known as **Metric Learning**.

## 3. Metric Learning

With the help of local consistencies (cf. FDH-2-7), we can write:
- (Ai - Bi) > (Ai - Ci)
- S (Ai, Bi) > S (Ai, Ci) in R.
- S (Ai, Bi) - S (Ai, Ci) > 0

Assuming this, the **hinge loss function** can be used as a cost function to compute the similarity "difference" between image triplet A-B-C (ie between images A and B, and images A and C). The metric can then be retro-propagated such as to bend the vector space on the basis of visual connections between given examples. Naturally, the larger the number of example triplets (Images A, B, and C), the more the space transformation is accurate.

One drawback of this system is the **erasure of spatial information** (in terms of scale, composition, etc). To reintroduce spatiality constraints in the similarity function, a heuristic coarse spatial reranking can be used.

Overall after all these metric learning steps, the **system has learned new invariants** specific to painting similarities, by understanding for instance to ignore textural features (eg. oil painting vs. woodcut).

## 4. Searching in collections: the Replica engine
Let's leave theoretical considerations aside for moment, and go back to the more practical issue of having a database searchable and usable by all.

In the case of the Cini collection, from the initial IIIF collection containing all digitised cardboards a second (simplified) IIIF system was extracted, this time with only the photographs (which had been segmented from the cardboards). The combination of these two IIIF servers can then be used in a search server, developed to mine text and images in queries (including algebraic queries, ie. combining several images in positive and negative), and represent the results as 2D maps.

## 5. Conclusion
### 5.1. Summary

Image analysis pipeline permit to construct the morphograph in a semi-automatic manner and recognise incoherent attributions.

### 5.2. In the next chapter

Like for text, the next chapter concern knows knowledge extraction out of images.

## Further reading

- Seguin, B. Striolo, C., di Lenardo, I. and Kaplan. F. (2016) Visual Link Retrieval in a Database of Paintings, VISART Workshop, ECCV, Amsterdam, September, 2016
