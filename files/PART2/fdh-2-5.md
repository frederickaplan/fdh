---
title: 'Foundations in Digital Humanities 2.5'
subtitle: 'Text Processing'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Text Processing

## Theses

1) Digital Humanities is the only field to deal with large collection of digital texts originating form collective discourses, massive digitisation and/or collective transcription projects

2) These large textual objects can be processed to extract hidden regularities and structures.

3) Some of these patterns and signatures are diachronic others are synchronic

4) The geometry of complex meaning spaces can be reconstructed even if we stay only at the surface of textual data.  

## Large textuals objects

### Humanities Computing, Computational Linguistics and Digital Humanities

Humanities Computing and Computational Linguistics were, and to some extent, still are different fields - with separate conference, societies, journals.

This can be traced back to to the origins of the two domains. Digital Humanities felt with philology and literature whereas Computationsal Linguistics was anchored in formal linguistics and computer science (we have see previously that both are hight linked, in particular though the work of Chomsky).

Progress in more formal foundation of the Digital Humanities permits to go beyond this field distinction.

Digital Humanities deals with large digital cultural objects and therefore with Large collections of Digital texts.

No other disciplines deal with these objects.

Humanities Computing, Computational Linguistics and Digital Humanities

### Some order of magnitudes

One page of a book contains 2000 - 3000 characters

A 400 pages book contains between 8.10^5 and 12.105 characters, so roughly 10^6, a million of characters

If you read 1000 books in your life, you will have read 10^9, a billion characters.

The Library of Congress contains 12.10^6 books, 12.10^12 characters.

Let's consider an alphabet of 32 characters (including spaces and punctuation). 32 is nice, because sqrt(1000) is 31.6, so more or less 32

Imagine now a text made of random characters

The character a1 would appear on average every 32 characters.

The sequence a1a2 every 32 *32 roughly 1000 characters.

The sequence a1a2a3 every 32^3 roughly 3.10^4 characters.

The sequence a1a2a3a4 every 32^4 108 characters, once or twice in a 400 page book.

A 6 characters chain would appear every 32^2.10^6 so roughly 10^9 characters, once in a lifetime. A 9 characters once in the entire Library of Congress

Obviously, texts are not random sequences. They possess strong regularity.

The study of this regularity is the subject of Linguistics. Linguistics try to describe texts in a more compact way by showing they possess regularity.

Syntactic trees and grammatical transformations are in fact compression algorithms.

But some far, Linguistics could never see its object at its full scale. Language structures were only captured from extremely partial information compared to information potentially available.

### Digital databases of historical texts

These large collections of digital texts originated from different sources

1) Large collective discourses (Twitter, Wikipedia)

2) Collection of historical texts either from digitisation projects or collective transcription and editing project.

Text processing pipeline

\> Physical document with a text written in a given script

\> Image of the Physical document

\> Extraction of the text based on reverse engineering of the writing system

\> Aggregation in the collection of digital texts

\> Possible transformation of the texts in other digital objects

Several projects exist.

Some are based on collective editing.

Other of highly automated transcription pipelines.

These large collection of historical texts are challenging because they contain texts originating from different places and times, redocumented and recontextualized several times.

#### Project Gutenberg

Founded in 1971 by Michael Hart with the aim of creating electronic books 60 000 ebooks -More 150 000 downloaded per day

Project Gutenberg is intentionally decentralized. There is no selection policy dictating what texts to add. Instead, individual volunteers work on what they are interested in, or have available.

Proof-reading is done with volunteers.

Michael Hart: “The goal of the project is "to provide as many e-books in as many formats as possible for the entire world to read in as many languages as possible”

A project slogan is to "break down the bars of ignorance and illiteracy”

“We do not write for the reader who cares whether a certain phase win Shakespear has a “:” or a “;”. We put our sights on a goal to release texts that at 99.9% accurate in the eye of the general reader”

#### Wikisource

Started in 2003 (first called Sourceberg)

Exist in 70 languages (with a subdomain like [fr.wikisource.org](http://fr.wikisource.org))

Edition tools facilities

#### Google Books

We saw the story of Google Books in past course.

The project use an automated scanning and OCR workflow, which is necessarily producing errors.

#### Impresso

76 newspapers collected,

600,919 issues,

5,429,656 pages scanned,

47,798,468 content items identified,

3,462,799 images,

12,493,358,703 words.

530,086 named entities disambiguated

#### Other projects

\- HathiTrust https://www.hathitrust.org

\- TCP (Text Creation Partnership) : https://textcreationpartnership.org

\- Historical Corpora (Arabic, Chinese, Dutch, French, Ancient English, German, Nordic Languages, Latin and Ancient Greek, Portuguese)

#### Project-based corpora

In his book *Enumerations*, Andrew Piper studies a corpus composed of :

230000 poems

15000 novels

12000 work of non fiction

This represents 1.4 billion words or 650 000 fictional characters.

## Diachronic evolutions

### Representativity of corpora

Homogeneity vs Size : Large textual corpus (e.g. Google Books) are heterogenous but their size makes them potentially more representative that others.

For a given year,

O : Set of all words said in French in the world

E : Set of all the words written in French in the world

P: Set of all the words written in the Press in the world

JDG : Set all the words used in the Journal de Geneve

GDL : Set of the words used in the Gazette de Lausanne

### n-grams

A n-gram is traditionally define as a sequence of n consecutive words.

(Sometimes a sequence of n consecutive characters)

N-grams can be counted using indexes.

For each years, one count how many times a given n-grams is appearing.

Google N-gram Viewer. Based on «google books» in several languages

Culturomics ([www.culturomics.org](http://www.culturomics.org))

Michel, Jean-Baptiste et al. 2011. “Quantitative Analysis of Culture Using Millions of Digitized Books” Science 331: 176-82.

In order to not have issues with copyright, some words have been suppressed from the index to be sure they cannot be used to reconstruct the texts.

Only the “Shadow of the texts” is indexed

N small are common to many contexts

N large rapidly unique

Some general "laws"

- Frequence of n-grams based on their rank
- Benford Law for word-numbers

Chronographs

Multi-scale diachronic analysis

Flat linguistics : Multi-scale n-gram analysis analyses lexicon dynamics, evolution of syntax but also pragmatics. These levels which are usually separated are flatten. It is an invitation to think beyond the sentence, beyond the syntax.

### Text reuse

Studying the presence of large portion of text (n-grams with n large) leads to the domain of Text Reuse.

Many authors borrow, with little or no transformation long part of texts from other sources.

Thus, text reuse algorithm permits to establish filiation and genealogies between texts.

The most interesting part of Text Reuse concern meaningful reiteration of text, beyond the simple repetition of common language.

In the academic context, text reuse can be associated with plagiarism.

In the context of literary studies text re-use is synonyms for literary phenomena like allusions, paraphrases and direct quotations.

Matteo Romanello, Aurélien Berra, Alexandra Trachsel. Rethinking Text Reuse as Digital Classicists. Digital Humanities conference, 2014

Smith, David A., Ryan Cordell, et al. “Computational Methods for Uncovering Reprinted Texts in Antebellum Newspapers.” American Literary History, vol. 27, no. 3, 2015, pp. E1–E15, doi:https://doi.org/10.1093/alh/ajv029.

Smith, David A., Ryan Cordel, et al. “Detecting and Modeling Local Text Reuse.” IEEE/ACM Joint Conference on Digital Libraries, 2014, pp. 183–92, doi:10.1109/JCDL.2014.6970166.

### Regular expressions

A regular expression (regex) is a sequence of characters that define a search pattern.

Each character in a regular expression (that is, each character in the string describing its pattern) is either

 \- a metacharacter,

\- a regular character that has a literal meaning

 '.' is a metacharacter that matches every character except a newline

For instance ‘DH.’ Matches ‘DHI’, ‘DHL’, etc.

[a-z] (match all lower case letters from 'a' to 'z') is less general than ‘.’

Regular expressions originated in 1951, when mathematician Stephen Cole Kleene described regular languages using his mathematical notation called regular events.

Complicated regexes arose in Perl in the 1980s, which originally derived from a regex library written by Henry Spencer (1986), who later wrote an implementation of Advanced Regular Expressions for Tcl.

Today, regexes are widely supported in programming languages, text processing programs

**Regular expressions** can be used to define complex criteria for the **n**-**grams,** thus extending in a very powerful manner the kind of analysis that can be performed.

## Distributional approaches

### TF-IDF

TF-IDF (term frequency–inverse document frequency), is a numerical statistic that is intended to reflect how important a word is to a document in a collection or corpus

Often used as a weighting factor

Term Frequency : The weight of a term that occurs in a document is simply proportional to the term frequency.

Inverse Document Frequency : The specificity of a term can be quantified as an inverse function of the number of documents in which it occurs.

If you just sort words based on how frequently they are used tf (t; d), you will get the usual the, and, etc.

TF-IDF scores the words based on how special they are to a particular document within the larger corpus.

### Word Matrix

• I like deep learning.

• I like NLP.

• I enjoy flying.

Similar Words have similar rows

Many matrices are possible

Chris Potts, Distributional approaches to word meanings, 2013

### From Latent Semantic Analysis to Topic Modeling

Topic modeling provides a suite of algorithms to discover hidden thematic structure in large collections of texts. The results of topic modeling algorithms can be used to summarize, visualize, explore, and theorize about a corpus.

LSA (Latent Semantic Analysis) uses TF-IDF scores in a larger term-document matrix.

Every word in the corpus is a different row in the matrix, each document has its own column, and the tf-idf score lies at the intersection of every document and word. This is a sparse matrix (mostly filled with zeroes).

LSA uses singular value decomposition to figure out how each word is related to every other words.

Probabilistic Latent Semantic Analysis was introduced by Puzicha and Hofmann (1999)

An additional layer between words and documents is introduced : topics.

Topics do not really exist... but can turn out to be a useful abstraction.

pLSA discovers topics, attaches them to a list of words, and classifies the documents based on those topics

Blei et al. (2003) improved upon this idea by turning into a generative model of documents, called Latent Dirichlet allocation (LDA)

The key new idea is the generative model.

Step 1: Choose a series of topics and their proportion in the book.

Step 2: Pick words from each topic based on their distribution.

... You are done.

If you can generate a document using this model, you can also reverse the process and infer, given any new document and a topic model, what the topics are that the new document draws from.

A topic is a probability distribution over words in the vocabulary.

The words distribution in a document reflects the topics it covers.

More precisely,

1) If you have a collection of documents, and you assume they are generated from latent

topics…

2) ... you assume documents are generated sampling topics and then sampling words from

topics (generative probabilistic modeling setting). Essentially we assume a joint

probability distribution over hidden (topics, topic proportions for each document, topic

assignment of each word in each document) and observed variables (words for

documents).

3) and you use the observed documents to infer the hidden topic structure that generated

them. Essentially we want to estimate the posterior of the hidden variables given the

observed variables.

Some references :

http://mimno.infosci.cornell.edu/topics.html

Implementations:

MALLET (Java): http://mallet.cs.umass.edu/

Gensim (Python): https://radimrehurek.com/gensim/

List of implementations in most languages:

http://www.cs.princeton.edu/~blei/topicmodeling.html

Tools:

Stanford Toolbox: http://nlp.stanford.edu/software/tmt/tmt-0.4/

Voyant tools: http://voyant-tools.org/

### Vector Space Models

One-hot representation model :

\- Words are regarded as atomic symbols

\- … coded using vector with one 1 and lot of zero

(0 0 0 0 0 1 0 0 0 0 0)

\- in a very large vector space

Results of Word spaces directly depends on the size of the corpus chosen (all the novel of the 20th century, all the novels and non-fiction works for the 17 to 20th century …)

Context is perspectival. It can change.

Size of Word spaces

20K (speech)

50K (normal vocal)

500K (big vocab)

3M( Google Model)

### Word embeddings

Continuous, numeric, dense word representations learned from raw text.

Similar vectors mean similar words (cosine vector distance)

Embeddings are a perfect input for numeric ML methods.

Embeddings can be obtained with Word Prediction Tasks (Word2Vec)

\- Hidden layer has dimensionality of embeddings

\- Input and output layer have dimensionality of one-hot-encoded

The model to automatically organize concepts and learn implicitly the relationships between them

Beyond Word Embeddings :

Of course you can extend the concept of Word Embeddings to n-gram embeddings, regular expression embeddings, word distribution (topic) embeddings ..

Word embeddings shows that there is a geometry of Word spaces, this can be used to align word embeddings in time and space.

### Diachronic Word embeddings

As we have seen, all documents are anchored on a moving ground : Language.

It is possible to calculate word embeddings for period of times and realign them

### Multi-linguistic spaces

(Tbd)

## Summary

Algorithms permit to extract patterns, trends and latent spaces out of large collections of text.

In the future, massive processing of large corpora may enable to model multiscale linguistic evolution in a spacetime continuum. The resulting linguistic simulator should permit to translate any “sentence” in space and time.

## In the next chapter

We will look at text understanding … trying to going beyond the surfacing features.

## Practice

SpaCy : https://github.com/allenai/scispacy

Solr : Search engine and index



## Further reading

- Jacqueline Leon, Histoire de l'automatisation des sciences du langage

- Aggarwal and Zhai, Mining Text Data

- Baayen, Analyzing Linguistic Data

- Ingersoll, Morton, Farris, Taming Text : How to find, organize and manipulate it.
