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

# FDH-2-4: Text Encoding

#### Theses

1) Widely accepted standards exist to encode characters.

2) For texts, a consensus hasn't been reached yet.

#### Contents
>1. Encoding Characters
>> 1.1. Early encoding of characters // 1.2. ASCII // 1.3. Unicode //
>2. Encoding Texts
>> 2.1. Non-hierarchical representations // 2.2. Hierarchical representations : XML // 2.3. Hierarchical represntation in DH. Focus: Text Encoding Initiative // 2.4. Beyond XML: Texts as Graphs and Born Digital Texts //
>3. Automatic transcription
>> 3.1. OCR and HTR // 3.2. Handling Spelling Variations //
>4. Conclusion
>> 4.1. Summary // 4.2. In the next chapter //
----
## 1. Encoding Characters

### 1.1. Early encoding of characters

The problem of encoding characters predates the digital age; and indeed, examples like Braille or Morse code show us that standardising the encoding of writing systems has long been debated.

But this question really took off with the explosion of computers, and digital representations in general.

### 1.2. ASCII

**ASCII** (American Standard Code for Information Interchange) was an early-stage coded character set developed in 1964, with each character being represented by 7 bits.

It was fine for encoding basic texts in English but not adequate for most other language in Latin scripts and obviously not adapted for languages in other scripts.

### 1.3. Unicode

The next stage in text encoding was **Unicode**: an 8, 16, or 32 bit encoded database of characters. The widely accepted standard, Unicode can handle 143,859 characters, covering 154 modern and historic scripts, as well as emerging characters (like emojis).

Unicode is **not concerned with Glyphs**. Unicode is instead concerned with Character (abstract unit of meaning) and not in principle concerned with Glyphs (specific shape, and therefore typefaces and fonts).

It is the function of the font to be this bridge between the Unicode-encoded character and the glyph printed on the screen. A font is "Unicode compliant" if the glyphs in the font can be accessed using code points defined in the Unicode standard.

#### Unicode and diacritics
Unicode considers diacritics (e.g. accents) as characters which have the property to combine graphically with base characters. Diacritic characters always follow the base character onto which they are applied.

As a principle of economy, any new character that can be created as a combination of existing character will not be newly encoded.

#### Unicode and new scripts
Unicode was progressively extended through the years and code points are now defined for almost any script — including runic, cuneiform, Linear B, Egyptian hieroglyphs.

Actually, the list of supported writing systems is in permanent expansion. Still, some rare medieval characters are challenging and various initiatives are continuously working to deal with them and include them in Unicode. This continuous updating of Unicode is one of its strength.

----
_With the unquestioned worldwide use of Unicode, the problem of a standardised character encoding system can be considered solved. The debate however remains for texts at large._

----

## 2. Encoding Texts

_What is a Text? Have we ever seen a Text; not a Document, but a Text_ per se _? When are two texts the same?_ It depends on the way the text is encoded.

We can consider different ways of modelling a Text using digital representations, remembering that we are dealing with a redocumentation process of something else, the "text in the world". Any digital representation of text, like **any redocuementation process, will be partial** (cf. FDH-1-3) and not completely accurate as something is always lost in the recollecting and remapping process.

### 2.1. Non-hierarchical representations

#### 2.1.1. Character chains

The simplest coding for a text is the just a **one dimensional** string, a sequence of Characters.

This is the traditional model of information theory (e.g. in the Turing machine metaphor).

This sequential representation cannot encode the structure, semantics, or link to external resources or references.

#### 2.1.2. "Bag of Words"

The text can also be considered as just a collection of words, indifferently ordered. With the bag of words representation, a text is just a set of words, disregarding grammar and even word order.

Most of the meaning is of course lost, and the only information retained is the number of occurence per word.

#### 2.1.3. Indexes

An index associating to each word its position can also be considered a text encoding.

Most indexes are not complete: no punctuation, limited precision on word position, etc. But if we imagine a _perfect_ index, then the entire text can be reconstructed losslessly.

It is an intermediary representation between the Bag of Words and the sequential chain.

Texts can indexed with different granularity of volumes (line, page, chapter, etc.)

Elements that are indexed can also varied : character, words, sequences of words.

Michael Witmore conceptualises the text as a "Massively addressable object". The book as a physical instance in one of the many levels of address, but this is not the only one.

The next chapter will look into details on how such indexes can be used to process texts.

### 2.2. Hierarchical representations : XML

#### 2.2.1. XML: A metalanguage
It is possible to encode part of the structure of the text in a slightly more elaborated textual encoding: **hierarchical representations**. We will study one of the best-known example of such encoding: XML.

Some complexity can be coded in a sequence of characters by patching them with so-called markup elements. XML stands for eXtensibile Markup Language. XML is actually used to create mark-up language. It is a **metalanguage**. XML is a W3C recommandation.

To write in XML you write text with tags : "\<a_tag> my text \</a_tag>". This can be done in any text editor, and in fact the simplicity of creating a new tag is one of XML's biggest strengths.

#### 2.2.2. Using XML: Four core ideas

1. XML is used to **describe data**, not to display them. XML does nothing. It describes.

2. XML tags are **not predefined**. You can define your own tags. This gives you a lot of freedom to describe the structure you want to describe.

3. When you are satisfied with your structure, you can fix your XML language by writing a DTD (**Document Type Description**). Thus, XML permits both fluidity and then rigour.

4. XML is, in theory, designed to be **self-descriptive** and “easily” readable. It is used to write “pivotal” descriptions in production chains _as an intermediary description between man and machine_.

#### 2.2.3. The History of XML
In the 50s, the first computers could not communicate with one another if they were from different brands. In an attempt to fix this, IBM created in the 60s GML (Generalized Markup Language) to enable data exchanges and make the data structure explicit.

This was a great success, so much that it became a standard, even adopted by the US government: SGML (Standard Generalized Markup Language)

In the 90s, Tim Berners-Lee at CERN creates the HTML language using a subset of SGML. HTML gets specialised in displaying data but does not impose a standard way for describing data.

A group of researchers imagines another language to do this. The first version of XML is ready in 1998. XML is meant to be a database in plain text.

#### 2.3.4. Syntax of an XML document

A well-formed XML document follows the general rules of XML syntax. It is, in essence, **formed like a tree** (hence the name of hierarchical structure), with substructures delimited by tags.

Even though it is not mandatory, most XML documents will follow the specific rules written in the Document Type Description. (Some software permit to check whether an XML file is valid compared to a given DTD.)

The XML file can then be **transformed** to be displayed; this process can be specified in a CSS stylesheet. More commonly, an XSLT script can be chained to transform XML content in iterative steps (for example into a different readable file format).

### 2.3. Hierarchical representation in DH. Focus: Text Encoding Initiative

_Why are we talking of XML in DH?_ Because of the TEI project. TEI is considered one of the most enduring and important project in the Digital Humanities community.

The **Text Encoding Initiative (TEI)** defines a a markup language for annotating texts with respects to their structural, visual and conceptual properties.

The TEI Guidelines provide many examples (and the corresponding DTD) for the representation of primary sources fo research and analysis. It is probably the **largest collection of XML schemata** in existence — and it is fully open.

#### 2.3.1. Structure of TEI documents
Just like XML, the TEI header contains the file description, a full bibliographic description of the computer file, an encoding description. The actual content contained in a <text> element with paragraphs and lists, quotations, bibliographic references, etc.

Specific modules are defined for particular text typologies (verse, drama, dictionaries), special documents (tables, formulas, graphics).

Like any XML-based system, TEI can be processed and displayed in numerous ways.

#### 2.3.2. The shortcoming of TEI
TEI has the ambition of describing the content of entire document. But, as we have seen, documents can have much more complex structures and circulations than XML trees.

TEI assumes that text are **Ordered Hierarchy of Content Objects (OHCO)**.

_But are all texts trees? Do all books have a tree-like structure?_

Scholars identify at least three disjointed hierarchies when reading the Bible:
- 1. A **reference** hierarchy: Testaments, books, chapter, verses

- 2. A **thematic** hierarchy: Pericopes, paragraphs, Sentences

- 3. A **layout** hierarchy: Pages, columns and lines.

Studies on the Bible may prefer each their own hierarchy. That's **the main flaw of XML: only one hierarchy can be documented**. If different hierarchies are to be documented, the only solution is to start the redocumentation process again, this time choosing another hierarchy.

Other limitations of TEI also include difficulties for mixing with binary data or pointing to external resources.

### 2.4. Beyond XML: Texts as Graphs and Born Digital Texts

_As a response to this problematic limitation, the recent years have seen grow new initiatives to overcome XML as the go-to solution in DH text redocumentation._

#### 2.4.1. TEF vs IIIF annotation

TEI has been developed in situation where a digital **facsimile is not available** and act as a standalone description of the document.

In recent years, the increase of the number of documents available has changed slightly the situation.

Part of the burden for describing the document can now be done as part of a IIIF manifest, which can **carry in a single object multiply-hierarchical information** and be linked to other documents in a complex network. TEI remains a possible textual format for describing  the textual content of some part of the document.

Part of the TEI effort for formalising historical textual content can be reinterpreted in this new context using the logic of Regulated Representations.

Graph modelling is well adapted to situation where texts need to be reconstructed out of multiple fragments.

These limitations pushed some (Thomas Efner) to suggest NoXML in DH (just like NoSQL in DataScience). What are the alternatives? What other representation can texts take?

#### 2.4.2. Text as Graphs

We've established that **a text is not a tree. _Could it be a graph?_**

Graphs have no problems with overlapping hierarchies.  Graph models suppress a number of the constraints that the database and markup models put on text modelling.

Graphs can also deal with the multidimensionality of text, and even with variants and ambiguity. This is especially crucial for old, fragmented texts, in which the structure is uncertain if not lost.

#### 2.4.3. Markov Models

An even more advanced model consist in considering texts as probabilistic graphs.

With Markov Models for instance, the textual representation can fully represent the uncertainty about the modelled text which, again, is especially convenient for fragmented sources.

By representing them as graphs, **texts become new objects**. These objects have lost readability but, as a tradeoff, can be interacted with — for example, if we want to show an alternative reconstruction of a text.
This text representation may not be very common, but it is a very powerful (open) representation of a textual object.

#### 2.4.4. Born Digital Texts
We've been talking about the transformation of physical texts into digital texts. But some texts are born digital.
Born Digital Texts have specific features:
- Hypertext
- Version management (like in Git) – whereby _text is considered as history_
- Some can be executed (e.g. Jupyter Notebooks, an executable mix of text and code).

They are also texts in themselves. They have their own semantics and semiotics. Knuth would consider code as executable literature (_Literate programming_), with its own style. And these born digital texts can be redocumented in other texts (transformed, summarized, indexed, represented, etc.).

#### 2.4.5. Version management of Born-Digital Texts: Texts as history

**_Not only is the text a network, it cam also become an history._**

Version management is one of the most interesting feature of text managed in digital platform (Github, Wikipedia). The text is encoded as an evolving historical object that **can be fully reconstructed** through a series of successive steps. This means that the text can be seen as **a series of actions**.

Side note: We'll see later that, more straightforwardly, buildings can be thought of as a series of actions; but that idea can be easily extended to all works of art, and these successive steps are not completely lost in physical objects (manuscripts, layers of paint, architectural details). But have to be reverse-engineered: great difference with born-digital texts, which has version management engraved in its DNA.

Every text, not just born-digital ones, are a history, the result of a series of successive changes. If one could, one would like to consider it as a full historical object.

Considering all textual objects as evolving entities is probably one of the most interesting step DH can do to reach a better modelling of what a text is.

---
## 3. Automatic Transcription

Automatic Transcription pipelines transform images into the digital model of a document (e.g. IIIF), including texts encoded using a given standard (TEI, XML or others).

The choice of the digital representation of the text defines the precise task that the algorithms need to perform.

### 3.1. OCR and HTR
#### 3.1.1. Optical Character Recognition

**Optical Character Recognition (OCR)** is said to be now **state of the art**, with most OCR techniques using language specific dictionaries but also syntactic modelling.

We have seen that **typefaces and spelling significantly changed** over time, which makes OCR still a challenge for historical texts. This challenge was recognised early. For instance in 1974, Ray Kurzweil created an early Omni-font OCR technology.

#### 3.1.2. Handwritten Text Recognition

Deep-learning based **Handwritten Text Recognition (HTR)** has made important progresses in recent years. The details of the methods will be discussed in the Algorithm parts.

#### 3.1.3. Importance of pre- and post-processing

OCR and HTR heavily rely on **pre-processing techniques** to segment and prepare texts. The way the machine learning problem is framed has a big impact on the successes of the algorithm.

The use of crowdsourcing can be used to correct texts. This can also be done in an indirect way (e.g. reCAPTCHA, finished in 2012 because the performances were too good).

#### 3.1.4. Computer Assisted Transcription

In computer assisted transcriptions, new interfaces help the transcription by detecting lines and words, and by suggesting possible transcriptions.

Big progress were made by the READ consortium and Transkribus interface. However, there are no “off-the-shelf” tool yet.

#### 3.1.5. Dealing with successive transcriptions

As OCR and HTR improve, the same document can lead to different text extractions. This create a general difficulty in processing pipelines.

If some conclusion are drawn out of the first transcription of a text (t1), these **conclusions need to be revised** each time the improvements of the transcription method yield a different (and better?) reading of the same text (t2, t3, etc).

Dealing with this **perpetual flow of information** is a big challenge in DH. A satisfactory pipeline should take an end-to-end approach and consider texts as intermediary, time-dependent, objects. This connects with what we hinted at earlier: the idea of text as history.

### 3.2. Handling Spelling Variations

(Most of this part from: _Michael Piotrowski, Natural Language Processing for Historical Texts, Morgan and Claypool_)

#### 3.2.1. Historical spellings and canonicalisation

In digital historical texts spelling may be different because:
- they differ from today’s orthography;
- they are inconsistent in their use;
- they have been transcribed with errors.


Words that have a common etymological origin are known as "**cognates**". The word *cognate* derives from the Latin noun _cognatus_ i.e. "blood relative”.
Expanding this definition, a "**canonical cognate**" is the equivalent of an historical word which preserves the morphological root and the morphosyntactic features of the historical form (e.g. _Brothor -> Brother, faeder -> father_). Some historical words that have disappeared may not have a canonical cognate.

The redocumentation process that consists in mapping historical spellings to modern spelling is referred to as normalisation or **canonicalisation**. This process was introduced in the 19th century by German philologist Karl Lachmann, in a era where critical editions were homogenising the variable spelling of original manuscripts to canonical forms.

This is however different form mapping to a modern form of a the word.

#### 3.2.2. Indexing spelling variants

If we now imagine a scenario in which historical texts are indexed in search engines, spelling modernisation is relevant. Which spellings are to be included? How permissive should the query be, with regards to orthography?

One possibility is to expand in the number of queries in real-time when a search is done, to include historical variants, or to perform approximate matching.

Various methods for handling spelling variants include:
- Edit distance (Levensthtein) matching
- Rule-based search;
- Grapheme-to-phoneme converters;
- Text-induced corpus clean-up;
- _n-gram_ based methods.

But overall, the remapping of dated spelling is still an unsolved problem.

----
## 4. Conclusion
### 4.1. Summary

Digital technologies have made great progress to represent digitally handwritten or printed texts, in any language (past or present).

However, automatic transcription is still a challenge, notably with regards to improving transcriptions and the handling of spelling variants.

### 4.2. In the next chapter

We will see how to process large collection of texts.

---
## Questions and answers

**Are poems included in the TEI?** Cannot be encoded as plain text; need to account for rhythm, scansion, enjambements, etc. A completer, Frederic ?


## Further reading

- Michael Piotrowski, Natural language processing for historical texts,  Morgan and Claypool
- Knuth, Literate Programming
- TEI (tbd)
- LeCun, Y.,Cortes, C., andBurges,	C.J. (1998).	“The	MNIST database	of	handwritten	digits”.
- *DeRose, Steven J.; Durand, David G.; Mylonas, Elli; Renear, Allen H.: What is text, really? J. Computing in Higher Education, 1(2):3–26, 1990.*
- Catherine Marshall, Reading and Writing the Electronic Book, Morgan and Claypool
- Michael Witmore, Text : A Massively Addressable Object in Gold, Debates about Digital Humanities

## To improve

- Solution for OCRs : Tesseract, Google API. A table for comparing them ? 
- Challenges for OCR: Transparancy. Preprocessing with histograms (to suppress word in transparency)
- Multiple pages. Line detection. 
- List of text formats : Markdown, RST (Restructuredtext)