---
title: 'Foundations in Digital Humanities 2.4'
subtitle: 'Textual Encoding'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Textual Encoding

## Theses

1) For creating digital representations of these texts one needs to combine powerful digital typography and universal textual representations standards

2) Standard exist to encode characters and texts

3) Still, some dispute exist on how to do it. 

## Encoding Characters

#### ASCII

ASCII (American Standard Code for Information Interchange) was an early stage coded character set developed in 1964. 

It was fine for encoding basic texts in English but not adequate for most other language in Latin scripts and obvisouly not adapted for languages in other scripts. 

#### Unicode

Unicode is not concerned with Glyphs. Unicode is concerned with Character (abstract unit of meaning) and not in principle concerned with Glyphs (specific shape, and therefore typefaces and fonts). 

A font is "Unicode compliant" if the glyphs in the font can be accessed using code points defined in the Unicode standard.

Unicode considers diacritics (e.g. accents) as characters which have the property to combine graphically with the base character. 

Combining characters always follow the base character to which they apply. 

As a principle of economy, any new character that can be created as a combination of existing character will not be newly encoded. 

Unicode was progressively extent through the years and defines now code points for almost any scripts including runic, cuneiform, Linear B, Egyptian hieroglyphs. 

Still, some rare medieval characters are challenging and various initiatives are continuously working to deal with them and include them in Unicode. 

## Encoding Texts

#### XML

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

#### TEI

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

TEI has been developed in situation where a digital facsimilé is not available and act a standalone description of the document. 

In recent years, the increase of the number of documents available has changed slightly the situation. 

Part of burden for describing the document can now be done as part of a IIIF manifest. TEI remains a possible textual format for describing the textual content of some part of the document. 

Part of the TEI effort for formalising historical textual content can be reinterpreted in this new context using the logic of Regulated Representations 

#### Text as Graphs

(Tbd)

## Automatic Transcription

### OCR and HTR

OCR is said to be now state of the art.

Most OCR techniques use language specific dictionaries but also syntactic modelling.

We have seen that typefaces and spelling significatively change over time which makes OCR still a challenge for historical texts. 

This challenge was recognised early. For instance in 1974, Ray Kurzweil created an early Omni-font OCR technology. 

Deep-learning based Handwritten Text Recognition has made important progresses in recent years. The details of the methods will be discussed in the Algorithm parts. 

Pre and Post processing : OCR and HTR heavily rely on pre-processing techniques, to segment and prepare texts.

The use of crowdsourcing can be used to correct texts. 

This can also be done in an indirect way (e.g. reCAPTCHA)

Computer assisted transcription : New interfaces help transcribing by detecting lines and words and suggesting possible transcriptions. 

Big progress were made by the READ consortium and Transkribus interface. 

However, there are no “off-the-shelf” tool yet. 

### Handling Spelling Variations

(Most of this part from : Michael Piotrowski, Natural Language Processing for Historical Texts, Morgan and Claypool)

In digital historical texts spelling may be different because 

\- They differ from today’s orthography 

\- They are inconsistent in their use

\- They are been transcribed with errors. 

Canonical cognate : an equivalent of a historical word the preserves the morphological root and the morphosyntactic features of the historical form. 

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

Dondi, Printing Revolution 

Richard Sproat, A Computational Theory of Writing Systems

Michael Piotrowski, Natural language processing for historical texts,  Morgan and Claypool

McLuhan, The Gutenberg Galaxy





