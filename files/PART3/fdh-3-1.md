---
title: 'Foundations in Digital Humanities 3.1'
subtitle: 'Semantic Modelling'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document


---

# Semantic Modelling

## Theses

1) A formalism exists to represent atom of knowledge 

2) This formalism is at the intersection of database, logic and graph theory

3) It can be used to represent knowledge and meta knowledge (knowledge about knowledge)

## From Tables to Graphs

### Tabular data

Example : modelling venetian routes. 

The simplest kind of dataset, that everyone is familiar with, is tabular data.

Any data kept in table such as an Excel spreadsheet or administrative page of a Cadaster.

Tabular data when invented was a revolutionary technology. 

Data kept in table is easy to display, sort, print, edit. 

You might not even think of data in an Excell spreadsheet as modelled. But there are semantics in data table. Where ?

What is the obvious limitation with this kind of storage ?

You cannot search for routes that stay more than 2 days at Corfu. Sorting the columns does not capture the deeper meaning of the text entered. 

### Relational database

Relational databases are a possible solution. Many very mature product exist like Oracle DB, MySQL, PostgreSQL.

A relational database allows multiple datables to be joined in a standardised way. 

However, as your project goes, one may need to reformulate the tables, This is called schema migration. A painful process. 

For big databases, schema can get incredibly complex. 

There is a whole industry based on solving this reoccurring issue. 

How can we make future proof schemata ?

Coding properties as tables : With this mode of coding we can add easily new properties (Price of the route, Captain, etc.). The schema is future-proof. In addition the data about the data (i.e .the metadata, the name of the columns) is now part of the data itself. This is ideal for projects in Perpetual Beta.

Most importantly it makes a direct and simple connection with a well developed research field : logic

### RDF Triplets

(Subject Predicate Object)

The subject denotes the resource, and the predicate denotes traits or aspects of the resource, and expresses a relationship between the subject and the object.

(R1 departure Venice)

This is called a RDF statement, a triple, an atomic relation in a database. 

We can easily add : 

(R1 departure-date 2.7.1422)

Various notation : 

(subject predicate object)

⇔ {subject, predicat, object} 

⇔ predicat(object, subject)

This is equivalent to 

∃ object, ∃ subject, predicat(object, subject)

As RDF statements can be understood both as logic statements as parts of a graph, one can use any tools and ideas from logic and graph theory to manipulate them. 

Formally, collection of RDF graphs form labeled, directed multi-graph. 

### Identifiers

The nodes of the Graph are called Resources

Who one needs to coordinate multiple datasets it can become an increasingly difficult task to guarantee unique and consistent idenfiers for each node. 

R1 that we use in our database may mean something else in another database

Can we define a unique id for all the concepts and entities of the world ?

Cf. Umberto Eco, Vertige de la liste

For naming resource, RDF uses URIs (Unique Resource Idenfiers) and an optional Fragment identifier. 

URIs generalize the concept of URL (Universal Resource Locators), the string used to specify how web pages are retrieved. Anything, whether one can retrieve it electronically or not, can be uniquely identified in a similar way. 

Uniform Reserouce Locator (URL) locates something (e.g. a page, an image) on the web

Uniform Resource Identifier (IRI) identifies an entire on the Webb (ASCII)

Internationalised Resource Identifier (IRI) identifies an entity on the web (UNICODE)

Since URIs can identified anything as a resource, the subject of an RDF statement can be a resource, the object can be a resource and most importantly predicates are always resources

It is common in RDF to shorten URIs by assigning a namespace to the base URI and writing only the distinctive part of the identifier. 

The URI :

http://www.w3.org/1999/02/22-rdf-syntax-ns#type

Can be shorten 

rdf:type

### Serialisation

Different serialisation formats exist : 

RDF/XML (the most frequently used), 

RDFa (RDF in attributes),  

Turtle (a compact, human-friendly format),  

N-Triples (easy-to-parse, line-based format that is not as compact as Turtle). 

N-Quads ( for serialising multiple RDF graphs), 

JSON-LD (JSON-based serialization), 

N3 (permits to define inference rules), 

RDF/JSON (an alternative syntax for expressing RDF triples using a simple JSON notation).

HDT (Header, Dictionary, Triples) is a compact data structure and binary serialisation format for RDF that keeps big datasets compressed to save space while maintaining search and browse operations without prior decompression. http://www.rdfhdt.org/what-is-hdt/

### Vocabularies

A set of URIRefs is knows as a vocabulary

We can design a specific vocabulary for the maritime route example. 

There are also famous vocabularies

### Ontologies

An ontology provides a special vocabulary with which knowledge can be represented 

This vocabulary allows us to specify which entities will be represented, how they can be grouped and what relationship connect then together. 

(Venice isa Place), (Corfu isa Place), (Place haslat latitude) (Place hassling longitude) …

Now something beautiful : 

An ontology can be expressed as RDF triples and stored in a graph alongside the data it describes 

OWL (Web Ontology Language) is an ontology language layered on top of RDF and RDFs (RDF Schemata)

\- Terminology statements 

ex::Bridge rdf:type rdfs:class

Ex::Bridge rdfs:subcass ex:Place

Protégé is a software to create your own ontology. 

We will see some universal ontologies in the next course. 

### Queries

Semantic coding is all about asking bigger questions. 

Just as SQL provides a standard query language across relational databases, SPARQL (pronounce sparkle) provides a query language for RDF graphs. 

SPARQL queries attempt to match patterns in the graph and bind wildcard variables as it finds solutions 

Departure (?x1, Venice)

Captain (?x1, ?x2), Gender (?x2, Woman)

### Rules

hasParent(?x1,?x2) ∧ hasBrother(?x2,?x3) 

⇒ hasUncle(?x1,?x3)

SWRL (Semantic Web Rule Language)

Only partial implementation. 

This is the subject of course 3-3

## Metaknowledge

Metaknowledge is knowledge about knowledge

Expressed knowledge (RDF triples) is not in the same space as resources (URI). We can easily attach new information to resource but not to triples

It is not easy to represent metaknowledge like th origin or the uncertainly linked with an information 

To overcome this issue we need to introduce two levels of knowledge and use a trick. 

An expressed RDF can be transformed into three reified triplets 

(Rialto hasTimeSpan 1588-1591)

(S1 rdf:subject RialtoReconstruction)

(S1 rdf:predicate hasTimeSpan)

(S1 rdf:object 1588-1591)

We can add : 

(S1 metardf:reliability 0.8)

(S1 metardf:creator FredericKaplan)

Now our RDF store includes historical knowledge and knowledge about the creation of this historical process.

These kinds of meta information can document all the construction phase of the RDF Graph (whether realised baby humans or machines)

With this approach we can extract through queries the historical knowledge corresponding to some specific sources and thus create a possible historical reality. 

## Summary

We must not only model historical information but model each step of the construction of the historical process. Any graph is itself an historical entity. 

There is a need for a semantic framework capable of coding historical information and meta-historical information. 

Coding meta-historical information implies documenting the choice of sources, transcription phases, interpretation processes realised by humans or machines. 

## Further Reading

- Eco Umberto, Vertige de la liste

- Tim Berners-Lee, Weaving the Web

- Marhias Girel, Science et territoires de l'ignorance

  


## To improve

- Talk about JustGUI, Datafirst, Converting a CSV in RDF

- Example Druid : Data Stories as Notebooks