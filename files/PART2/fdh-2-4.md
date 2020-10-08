---
title: 'Foundations in Digital Humanities 2.4'
subtitle: 'Text Encoding'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Text Encoding

## Theses

1) Widely accepted standard exist to encode characters 

2) For texts, there are still some debates

## Encoding Characters

### Early encoding of characters

- Braille
- Morse code
- Telegraph

### ASCII

ASCII (American Standard Code for Information Interchange) was an early stage coded character set developed in 1964. 

It was fine for encoding basic texts in English but not adequate for most other language in Latin scripts and obvisouly not adapted for languages in other scripts. 

### Unicode

Unicode is an 8, 16, or 32 bit encoded database of characters. 

Unicode is not concerned with Glyphs. Unicode is concerned with Character (abstract unit of meaning) and not in principle concerned with Glyphs (specific shape, and therefore typefaces and fonts). 

A font is "Unicode compliant" if the glyphs in the font can be accessed using code points defined in the Unicode standard.

Unicode considers diacritics (e.g. accents) as characters which have the property to combine graphically with the base character. 

Combining characters always follow the base character to which they apply. 

As a principle of economy, any new character that can be created as a combination of existing character will not be newly encoded. 

Unicode was progressively extent through the years and defines now code points for almost any scripts including runic, cuneiform, Linear B, Egyptian hieroglyphs. 

Still, some rare medieval characters are challenging and various initiatives are continuously working to deal with them and include them in Unicode. 

## Encoding Texts

What is a Text ? When are two texts the same ? It depends on the way the text is encoded.

We can consider different ways of modelling a Text using digitral representations, remembering that we are dealing with a redocumentation process of something else, the "text in the world". Any digital representation of text, like any redocuementation process will be partial and not completely accurate as something is always lost in the recollecting and remapping process. (cf FDH 1-3)

There are different usages

Documents 1 > Text 1

Document 2 > Text 2

Comparison between Text 1 and Text 2

-

Documents 1 > Text 1 > Document 2 (e.g ebook)

-

Documents 1 > Text 1

Documents 2 > Text 2

…

Documents 3 > Text 3



Analysis of Text 1 .. Text n (Subject of next course)

### Character chains

The simplest coding for a text is the just a one dimensional string, a sequence of Characters. 

This is the traditional model of information theory.

This sequential representation cannot encode the structure, semantics, or link to external resources or references. 

### Bag of Words

With the bag of words representation, a text is just a set of words, disregarding grammar and even word order. 

The number of occurence per words is informed. 

### Indexes

An index associating to each word its position can also be considered a text encoding. If the positon is precise, the entire text can be reconstructed. 

It is an intermediary representation between the Bag of Words and the sequential chain.

### Hiearchical representations : XML

It is possible to encode part of the structure of the text in a slightly more elaborated textual encoding. : Hierarchical representations. 

We will study one example of such encoding : XML

Some complexity can be coded in a sequence of character by patching it with so-called markup elements. 

XML stands for eXtensibile Markup Language XML is a metalanguage for creating mark-up language. XML is a W3C recommandation. 

To write in XML you write text with tags : <atag> my text </atag>

This can be done in any text editor. 

1. XML is used to describe data, not to display them. XML does nothing. It describes.

2. XML tags are not predefined. You can define your own tags. This gives you a lot of freedom to describe the structure you want to describe.

3. When you are satisfied with your structure, you can fix our XML language by writing a DTD (Document Type Description). Thus, XML permits both fluidity and then rigor. 
4. XML is designed to be self-descriptive and “easily” readable. It is used to write “pivotal” descriptions in production chains

In the 50s, the first computers could not communicate with one another, if they were from different brands. 

In the 60s, IBM creates GML (Generalized Markup Language) to enable data exchanges and make the data structure explicit.

This is a great success. It becomes a standard : SGML (Standard Generalized Markup Language). The US fed gov. adopts it. 

In the 90s, Tim Berners-Lee at CERN creates the HTML language using a subset of SGML. 

HTML gets specialized in displaying data but does not impose a standard way for describing data. 

A group of researchers imagines another language to do this. The first version of XML is ready in 1998. XML is meant to be a database in plain text.

<BOOK>

 <FRONT>

  <TITLE>... </TITLE>

  <AUTHOR>...</AUTHOR>

 </FRONT>

 <BODY>

  <PART>

  <CHAPTER>...</CHAPTER>

  </PART>

 </BODY>

</BOOK>

A well-formed XML document follows the general rules of XML syntax.

A valid XML document follows the specific rules written in a DTD (Document Type Description)



<!DOCTYPE BOOK

[

<!ELEMENT BOOK (TITLE,AUTHOR,YEAR)>

<!ELEMENT TITLE (#PCDATA)>

<!ELEMENT AUTHOR (#PCDATA)>

<!ELEMENT YEAR (#PCDATA)>

]>

To use a DTD is not mandatory. But a DTD permits to agree on common XML dialect. 

Some software permit to check whether an XML file is valid compared to a given DTD.

The way an XML file is displayed can be specified in a CSS stylesheet.

A document can also be transformed using an XSLT script.

In a more general way, XSLT script can be chained to transform XML content in iterative steps. 

### TEI

TEI is considered one of the most enduring and important project in the Digital Humanities community.

The Text Encoding Initiative (TEI) defines a a markup language for annoting texts with respects to their structural, visual and conceptual properties. 

The TEI Guidelines provide many examples for the representation of primary sources fo research and analysis.

A DTD is provided.

It is probably the largest XML schemata in existence.

… and it is fully open.

The TEI header contains the file description, a full bibliographic description of the computer file, an encoding description.

The actual content contained in a <text> element with paragraphs and lists, quotations, bibliographic references, etc. 

Specific modules are defined for particular text typologies (verse, drama, dictionaries), special documents (tables, formalulas, graphics)

TEI like any XML based system can be processed and displayed in numerous ways. 

TEI has the ambition of describing the content of entire document. But,as we have seen, document can have much more complex structure and circulation than XML trees. 

TEI assumes that text are Ordered Hierarchy of Content Objects (OHCO) 

*DeRose, Steven J.; Durand, David G.; Mylonas, Elli; Renear, Allen H.: What is text, really? J. Computing in Higher Education, 1(2):3–26, 1990.*

The Bible has at least three disjointed hierarchies relevant for scholars

\- A reference hierarchy: Testaments, books, chapter, verses

\- A thematic hierarchy : Periscopes, paragraphs, Sentences

\- A layout hierarchy : Pages, columns and lines. 

It is not a simple tree. 

Other limitations of TEI: Difficulties for mixing with binary data or pointing to external resources. 

TEI has been developed in situation where a digital facsimilé is not available and act a standalone description of the document. 

In recent years, the increase of the number of documents available has changed slightly the situation. 

Part of burden for describing the document can now be done as part of a IIIF manifest. TEI remains a possible textual format for describing the textual content of some part of the document. 

Part of the TEI effort for formalising historical textual content can be reinterpreted in this new context using the logic of Regulated Representations 

### Text as Graphs

A text is not a tree. Is it a graph ?

Graphs have no problems with overlapping hierarchies.  Graph models suppress a number of the constraints that the database and markup models put on text modeling.

Graphs can deal with the multidimensionality of text. Graphs can deal with variants and ambiguity. 

### Markov Models

An even more advanced model consist in considering Text as probabilistic graphs.  

With Markov Models for instance, the textual representation can fully represent the uncertainty about the modelled text.

Link with the way Markov Models have been used in Speech2Text. 

### Born Digital Texts

Born Digital Texts have specific features 

\- Hypertext

\- Version management 

\- Some can be executed (e.g. Jupyter Notebooks)

They are also texts in themselves. They have their own semantics and semiotics. Knuth would consider code as executable literature (Literate programming)

And these born digital texts can be redocumented in other texts. 

Version management is one of the most interesting feature of text managed in digital platform (Github, Wikipedia). The text is encoded as an evolving historical object that can be fully reconstructed through a series of successive steps. 

### Texts as history

The text is an history.

When you thing about it this is true for every texts. Every text is the result of writing and transformation process. If one could, one would like to consider it as a full historical object. 

Considering all textual objects as evolving entities is probably one of the most interesting step DH can do to reach a better modelling of what a text is. 

## Automatic Transcription

Automatic Transcription pipelines transform images in a digital model of a document (e.g. IIIF), including Texts encoded using a given standard (TEI, XML or others). 

The choice of the digital representation of the text defines the precise task that the algorithms need to perform. 

### OCR and HTR

OCR is said to be now state of the art.

Most OCR techniques use language specific dictionaries but also syntactic modelling.

We have seen that typefaces and spelling significatively change over time which makes OCR still a challenge for historical texts. 

This challenge was recognised early. For instance in 1974, Ray Kurzweil created an early Omni-font OCR technology. 

Deep-learning based Handwritten Text Recognition has made important progresses in recent years. The details of the methods will be discussed in the Algorithm parts. 

Pre and Post processing : OCR and HTR heavily rely on pre-processing techniques, to segment and prepare texts.

The use of crowdsourcing can be used to correct texts. 

This can also be done in an indirect way (e.g. reCAPTCHA, finished in 2012 because the performance were too good)

Computer assisted transcription : New interfaces help transcribing by detecting lines and words and suggesting possible transcriptions. 

Big progress were made by the READ consortium and Transkribus interface. 

However, there are no “off-the-shelf” tool yet. 

How to deal with successive transcriptions : As OCR and HTR improve the sane document can lead to different text extractions. This create a general difficulty in processing pipelines. 

Document 1 > Text 1 (t1)

Document 1 > Text 1 (t2)

Document 1 > Text 1 (t3)

If some conclusion are drawn out of Text 1 (t1) these conclusions needs to be revised. 

A satisfactory pipeline should take an end-to-end approach and consider texts as intermediary, time-dependent, objects. Text as history. 

### Handling Spelling Variations

(Most of this part from : Michael Piotrowski, Natural Language Processing for Historical Texts, Morgan and Claypool)

In digital historical texts spelling may be different because 

\- They differ from today’s orthography 

\- They are inconsistent in their use

\- They are been transcribed with errors. 

Cognates : Words that have a common etymological origin. The word *cognate* derives from the Latin noun cognatus i.e. "blood relative”

Canonical cognate : an equivalent of a historical word that preserves the morphological root and the morphosyntactic features of the historical form. (Brothor > Brother, faeder -> father)

Some historical words that have disappear may not have a canonical cognate. 

The redocumentation process that consists in mapping historical spellings to modern spelling is refered to as normalisation or canonicalisation. 

This process was introduced in the 19th century by German philologist Karl Lachmann. Critical editions were homogenising the variable spelling of original manuscripts to canonical forms. 

This is however different form mapping to a modern form of a the word. 

When indexing historical text in search engines, spelling modernisation is relevant. 

One possibly is to expand in the number of queries in real-time when a search is done, to include historical variants, or to perform approximate matching. 

Various methods 

\- Edit distance (Levensthtein) matching

\- Rule-based search

\- Grapheme-to-phoneme converters

\- Text-induced corpus clean-up

\- n-gram based methods

## Summary

Digital technology have made great process to represent digitally handwritten or printed texts in any language of works (past or present)

Automatic transcription is still a challenge but great progress are made. 

## In the next chapter 

We will see how to process large collection of texts

## Further reading

- Michael Piotrowski, Natural language processing for historical texts,  Morgan and Claypool

- Knuth, Literate Programming 





