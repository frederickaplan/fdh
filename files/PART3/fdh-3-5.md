---
title: 'Foundations in Digital Humanities 3.5'
subtitle: 'Topological Data Science'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Topological Data Science

## These

1) Non conceptual knowledge systems are not black boxes. They can be fully inspected and analysed. 

2) Topological Data Analysis deals with the “shape of data” to give us insight on the underlying structure of these knowledge spaces.

3) We can get some intuition of the structure of these giant shapes by understanding well what some mathematical notion in lower dimensions. 

## Mathematical roadmap

Most of machine learning is built upon three pillars: linear algebra, calculus, and probability theory.

Calculus and linear algebra can be studied independently, as is usually the case in a standard curriculum.

Calculus is the study of differentiation and integration of functions. Essentially, a neural network is a differentiable function, so calculus is a fundamental tool to train neural networks.

Neural networks are essentially functions, which are trained using the tools of calculus. However, they are described with linear algebraic concepts like matrix multiplication.

Linear algebra deals with vector spaces, normed spaces, linear transformation, matrices, determinant, eigenvalues, eigenvectors and matrix decompositon.

 Multivariate calculus is the part where linear algebra and calculus come together, laying the foundations for the primary tool to train neural networks: gradient descent. 

Mathematically speaking, a neural network is simply a function of multiple variables. (Although, the number of variables can be in the millions.)

Probability theory is the mathematically rigorous study of chance, fundamental to all fields of science.

Two core concepts are important for neural network : expected value and entropy.

These are the basic mathematical foundations for all non-conceptual knowledge system. 

They permits to build system and understand how they work but they may not be sufficient for what interest us : understanding the structure and shape of non-conceptual knowledge systems. 

For this, another mathematical branch can be useful : Topology and more specially Topological Data Analysis. 

## Undertanding the Shape of Data

### Manifolds

Gauss (1777-1855) is probably the first to have considered abstract spaces as mathematical objects. 

His **theorema egregium** (1827) gives a method for computing the curvature of a surface without considering the ambient space in which the surface lies.

Such a surface would, in modern terminology, be called a manifold.

A a manifold is a topological space that locally resembles Euclidean space near each point. 

The dimension of the manifold corresponds to the degree of freedom on which one can move on this surface. (2 for a map)

A manifold is a connected region, as set of points associated with a neighbourhood around each point. For any given point the manifold appears to be a Euclidean space. We experience the surface of the world as a 2-D plane but is in fact a spherical manifold in 3-D space. 

Example of 3D manifold : Sphere, Torus, Klein Bottle

More complex manifolds exist like Riemann surfaces. 

### Manifold hyphothesis

The manifold hypothesis states that in many cases such as the case of natural images the support distribution is concentrated on low dimensional manifolds in an Euclidean space. The high-dimensional data lie on low-dimensional manifolds embedded within the high-dimensional space.

As the actual data set of interest actually lives on in a space of low dimension, a given machine learning model only needs to learn to focus on a few key features of the dataset to make decisions.

The manifold hypothesis tries to explain why the system can learn despite the dimensionality curse. 

### Topology

Topology is the branch of mathematics dealing with the geometric properties of shape. 

The studies properties are coordinate invariant, deformation invariant. Topological properties do no change when twisting, strechting, pulling 

They can be interpreted as compressed representation of family of possible shapes. 

Different Glyph of A can be similar to the character A from a topological point of view. 

### Topological Data Analysis

G. Carlsson Topology And Data, Bulletin (New Series) of the American Mathematical Society Volume 46, Number 2

Topological Data Analysis deals with the “Shape of Data”.

Topological Data Analysis has extended Algebraic Topology, a branch of mathematics that uses tools from abstract algebra to study topological spaces, to allow a mathematically rigorous study of “shape”. 

Traditional analytics works in low dimensionality and assumes a model of behaviour 

Topological Data Analysis work in high dimensionality and assume only a measure of similarity (like a distance)

Topological Data Analysis constructs a network in which every node contains a subset of your data, and two nodes are connected to each other if they share some data. It represents the shape of data in a combinatorial form, that is very easy to compute and process. 

### Persistent homology

The main tool of Topological Data Analysis is **persistent homology.** 

Persistent homology deals with the stability of features that one discovers using topological methods. 

Persistent homology deals with the notion of components, holes, tunnels, cavities, and so on and quantifies their “significance”.

Fourier analysis : signal 

persistent homology : shape

Example : How can we compare mountains and volcanoes?

Mountains are local maxima of the function

Knowing there is maybe noise on the function, what is the real shape of the mountains ?

How can we characterise the special shape of volcanoes ?

Idea: Characterising the shape using sea-level rise

Let’s call Uc the shape above the see level c. 

Persistant homolgy keeps tracks of the evolution of Uc as c declines

### Homology groups 

For any topological space X the so-called ith homology groups Hi are introduced. The actual number of i-dimensional holes in X is given the rank of Hi, the concept which is quite similar to the dimension of a vector space. 

These ranks are called the Betti numbers.

H0: 0 dimensional holes (Clusters)

H1 : one dimensional hole (Cycles, Loops)

H2: two dimensional hole (Voids,Hole)

### Persistence diagram

General idea : 

Constructing a so-called simplicial complex as a finite collection of n-simplices

Monitoring when various shape appears (cycles, etc.) and producing a **persistence diagram** 

Given a data set, collection of points embedded in some space, there exist different way of contracting a n-simplex (Rips complex, Cech complex)

Birth and death of features : 

As d increases, a hole appears between d1 and d2. 

The pair (d1,d2) is called the persistence of hole. 

The persistence diagram permits to detect a stable signature for shape.

Robert Ghrist. Barcodes: the persistent topology of data. Bull. Amer. Math. Soc. (N.S.), 45(1):61–75, 2008

Aims 

\- detect inter-layer mapping in feed forward nets

\- characterise the inner structure of embeddings 

\- characterise data structure for GAN application. 

### Witness complexes

Comparing the structure of manifolds

Computing persistant barcode could be challenging for large dataset. 

One possibility is to use a small subset of landmark points is chosen and a simplicial complex is constructed using these points as vertices (witness complexes)

- - De Silva, V. and Carlsson, G. E. Topological estimation using witness complexes. SPBG, 4:157–166, 2004.

There are various strategies for sampling the best landmarks (random, minimax (risk of sampling outliers))

### Relative Living Times

Instead of comparing persistent barcodes (quite complex objets), one can use compute the Relative Living Times (RLT) of each number of holes that was observed. They are defined as the ratio of the total time when this number was present and of the value max when points connect into a single blob.

Ex: 50% of all period of topological activity we have observed that there is at least 1 one-dimensional hole

On this basis one can compute the Mean Relative Living Time MRLT(i; k;X) as a probability distribution (over integers).

It is possible to compare distribution simply with the L2 distance

Ex: for GANs

## Topological analysis and Logic

Topological Techniques for understanding the shape of data are echoing the morphological techniques we discuss to model shape in a procedural manner in Part II. 

Shape understanding is at the heart what Digital Humanities try to achieve. 

Topological Signal Processing : Based on sheaf theory. A sheaf is a mathematical data structure to store local information over a topological space

Sheaves and Geometry and Logic : Link with topic theory (incorporate thinking, perception and logic). The logic is in the structure of the data. 

Topos Theory : Alexander Grothendieck (1928 -2014) on algebraic geometry. Over 20,000 pages of Grothendieck's mathematical and other writings, held at the University of Montpellier, remain unpublished. One of its central invention, the topos are now considered one of the bridge that can unify mathematics. They can play a crucial role for understanding Shape of Data. 

## Summary

Topogical analysis permits to analyse the shape of data helping characterise non conceptual knowledge. 

Data has structure which permits to make a link with logic. 

Understanding this relation between shape and logic is at the heart of the problem Digital Humanities needs to solve. 

This will be a crucial step for founding Digital Humanities in solid mathematical framework. 

## Further Reading

