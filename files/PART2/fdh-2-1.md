---
title: 'Foundations in Digital Humanities 2.1'
subtitle: 'Digitisation Processes'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# FDH-2-1: Digitisation Processes

#### Theses

1) Document digitisation is a problem of conversion of dimensions

2) Digitisation is logistic optimization

3) Optimization causes risks of alientation

4) Digitisation does not equate with an easier accessibility

5) As digitisation unlocks ivory towers, it faces many resistances

#### Contents
> 1. The Story of Google Books
>> 1.1. Figures // 1.2. Chronology //
> 2. Concepts
>> 2.1. From documents to digitised images // 2.2. The problem of dimensional conversion // 2.3. Digitisation as a logistics problem // 2.4. Optimisation prospects //
> 3. Conclusion
>> 3.1. Summary // 3.2. In the next chapter //
---

_We'll start with a story, one to be known, a story of challenges, resistence, but ultimately success: the story of Google Books._


## 1. The Story of Google Books

### 1.1. Figures

In October 2019, Google Books announced they had digitised **40 millions books**. This is far beyond other comparable initiatives: the Hathi Trust estimates to 17 million the number of books they digitised, while Gallica (the Bibliothèque Nationale de France's effort) remains around 0.7 million.

No matter how impressive Google's figure is, it remains little compared to the **271 million book files** listed in the OCLC / WordCat catalog, which aggregates data from the 1.8 billion books stored in 72,000 public and private libraries around the globe. In addition to that, almost 1 million new books are published each year.

To put these numbers in perspective, after having digitised its first million books, the Michigan Library announced that they were equivalent to :

- 25.8 km
- 680 tons
- 361 million pages
- 70 billion words
- 42 Terabytes
- 428 Languages

If we project those figures to Google's 40 million books, we get a glimpse of the **importance of logisitics** in any massive-scale digitisation process:

- 1,032 km
- 27,200 tons
- 14.4 billion pages
- 2.8 trillion words
- 1,680 Terabytes

Among these 40 million books, only a **subpart is online for copyright reasons**. Alain Jacquesson estimates that only 20% of the entire set is out of copyright as of today. Indeed, contrary to Gallica and other public book repositories, the largest part of the Google Books base is composed of commercially exploitable books. This will play a key role in the Google Books story.

### 1.2. Chronology

#### (1996-1997) Google and Books are intrinsically linked

Google Books is in Google's DNA. The beginnings of the company are tightly linked with the Stanford Digital Library Technologies Project. The initial goal was to build **"crawlers" to analyze book contents**.

Larry Page and Sergey Brin’s idea was to quantify the value of a book: this value was **based on how cited was the book, and, recursively, how cited were the citing books**. The relevance of a book was to be computed based on the quantity and the quality of the citations of this book in other books. The first algorithm to do this is called “BackRub”. It will be the basis of **PageRank**, the algorithm that made Google successful.

Four years after the creation of Google, a small team (including Marissa Mayer, future Google VP and then Yahoo CEO) started thinking again about a book-related project.

#### (2002-2003) Birth of a project: The Google Five

The first question raised was: how long would the digitisation of most of the world's books take? To answer this, Page and Mayer did simple page-turning experiments (with a metronome). The result was that 300 pages required 40 minutes.

Using this primitive benchmark, they started to tour the the most important digital libraries projects: Library of Congress, Gutenberg Project, Million Book project, etc.

Page approached the 5 most important libraries of the US, starting with the **University of Michigan Library**, where he had studied for his bachelor: a system of 19 libraries, containing 9.2 million volumes (in 2008), and acquiring about 180,000 new volumes per year.

While the library of Michigan estimated that it would take 1,000 years to digitise 7 million volumes, Page boldly announced that he could do this in only 6 years.

Larry Page then went to Stanford where he meets Terry Winograd, Paul Allen (co-founder of Microsoft), and Michael Keller (director of the Stanford Library). When Keller came to the GooglePlex in September 2003, Page offered to digitise the 9 million books contained in the **Stanford library** and to put them online.

By that time, Page was ready to approach the largest academic library in the world: the **Harvard University Library network**. Founded in 1638, it comprises 90 libraries; the main one, the Widener Library, counts alone 16 million volumes.

Sidney Verba, Harvard Libraries' president is sceptical about the technical aspects of the project, but is quickly impressed by Page's scanning machines at Mountain View. (Although, as a side note, Google will eventually not use automatic scanning machines.)

Despite the replacing of Verba in 2007 by the less-enthusiastic Robert Darnton, Harvard still moves forwards in Google's project.

Across the pond, Page finds in the **Univesity of Oxford's Bodleian Library** (founded in 1602 and having about 12 million books) a major European ally.

The last of the five initial partners was the **New York Public Library**, which holds 16 million documents. Its director, Paul Leclerc was then mostly interested in public domain and not too fragile books.

#### (2004) Project Ocean

Once these five initial "giant" paterns had been secured, Google started working on the technical aspects of the projects, under the direction of Susan Wojcicki. Little press is made of "Project Ocean" as it's known then.

However, a major turning point is approaching: Google rented a stand at the **Buchmess** in Frankfurt, where Page and Brin present the Google Prints for Editors project. They also mention the existence of a much larger project, called **Google Print**, but do not give details.

Nobody takes them seriously. The Frankfurter Allgemeine even ironically titles: _“The founders of Google have found an interest for books”_.

However, on the 14th of December 2004 happened the “earthquake” announcement of Google Print: a collaboration with 5 major libraries ("The Google 5"), owning together about 50 million books. The announcement of the digitisation of several million  (between 6 to 15) books in less then 10 years and of a collaborative program for publishers was met with **worldwide reactions** (both positive and negative).

In [_Anatomy of Aggregate Collections: The examples of Google Print for Librairies_](http://www.dlib.org/dlib/september05/lavoie/09lavoie.html), Brian Lavoie et al. tried to gauge (using complete WorldCat data) the redundancy of the available collections. They found not only that the older the book, the less likely it was to be stored in different collections, but more surprisingly that **very few common books were held in all 5 libraries**:
- 61% of books were in only 1 library;
- 20% of books common to 2 libraries;
- 10% of books common to 3;
- 6% of books common to 4;
- and only 3% of the books common to all 5 collections.

It thus appears that this was a **very wise initial choice of libraries**, which potentially saved a lot of money (as redundant digitisation is minimised). In addition to this, the linguistic diversity (430 languages, and only 50% of the documents in English) proved also advantageous.

Initially, **only 20 % of documents were in open-access**, but of course, as years pass, more and more works enter in the public domain. In the meantime, Google has a “war treasure”: once the copyright deadline for these 80% is reached and as digitisation progresses, Google Books is bound to become the world's largest public library.

This has put a lot of pressure on other actors, and has encouraged concurrent efforts (for example, the **Europeana project** started in 2008 by the European Union, although it has now diverged a bit from the digitisation of books and now acts as a cultural content aggregator).

#### (2005-2008) Extensions and issues

Progressively, Google Books added new features (Google Search, Places in books, Popular passages, etc.)  and started to expand towards Europe, with the addition of the:
- **University of California** system (34 million books)
- **University of Madrid** (First Spanish-speaking university)
- **University of Wisconsin-Madison** (7.2 million books)
- **University of Virginia** (5+ million books, 17 millions manuscripts)
- **University of Lausanne** (100 000 books from 17 to 19e century, First French-speaking library)
- A negotiating process with the **Bibliothèque Nationale de France** was also initiated.
- the **Bibliothèque de Lyon** was also signed onboard, with the caveat that French law requires the Google contract to be disclosed.

#### (2005-2015) Trials and class actions

Various entities (individuals and organisations) began to conglomerate in 2005 with the idea of attacking Google on copyright issues (the so-called _Authors Guild, Inc. v. Google, Inc._ class action).

As a first results, in 2009, the Google Book Settlement (GBS) structured the status of the books still in commercial books. The GBS allowed to continue the program by **paying for the works previously scanned and allowing authors and publishers to opt-out**.

This settlement is refused; and a new version, written in 2011 is also refused.

At the heart of the debate lied the question of **Opting-in** (asking each publisher for approval before digitising) **vs. Opting-out** (allowing all publishers to remove their content after the digitisation is complete). **Orphan works** (ie. works for which the copyright owner is unknown or unreachable), and the "grey zone" in which they lied and through which Google could exploit them, were also deemed problematic.

Nonetheless, in 2013, the District Court stated that the Google Books project met all legal requirements for **fair use** and declared:

_“Google’s unauthorized digitizing of copyright-protected works, creation of a search functionality, and display of snippets from those works are non-infringing fair uses. The purpose of the copying is highly transformative, the public display of text is limited, and the revelations do not provide a significant market substitute for the protected aspects of the originals. Google’s commercial nature and profit motivation do not justify denial of fair use._

_Google’s provision of digitized copies to the libraries that supplied the books, on the understanding that the libraries will use the copies in a manner consistent with the copyright law, also does not constitute infringement.”_

This court decision paved the way for the growth in the number of books digitisation projects around the world.

---
## 2. Concepts

### 2.1. From documents to digitised images

Straightforwardly, the document digitisation process transforms material documents into digital images. It is, however, a **complex process which combines human and machine intervention**.

For us to understand this complex transformation well, we should ask ourselves two fundamental questions:
- **What is a document ?**
- **What is a digital image ?**

#### 2.1.1. What is a document?

A document is a **record resulting from an inscription process** (whether through text, image, or sound). A document is therefore unthinkable without the act of documenting, which consists in some **material inscription** that lasts through some time.

To produce a document is to **produce an object different** to the documented object.

Documents have a performative dimension: they act in the world. It is therefore important not only to study their form, but also understand their function.

#### 2.1.2. What is a digital image?

Digitisation is often the **documentation of a document** (when, for example, an analog photography is recaptured digitally). The produced digital image is the result of a complex algorithm and a particular hardware.

This makes a digital image often more difficult to interpret, if the information about the used software and hardware is not provided.

Regarding hardware, many typologies of cameras exist today. Examples include: cameras with colour filters for visible light, or multispectral cameras which can be adapted to specific digitisation missions (Ultraviolet for surface imaging, or Infrared for subsurface imaging, for example).

### 2.2. The problem of dimensional conversion

Digitisation pipelines can be thought conceptually as a dimension conversion problem.

For example, the transcription of a book can summarised as going:
- **[3D]** from a book, on a shelf, in a building;
- **[2D]** by choosing a page, and digitising its images and texts;
- **[1D]** to a series of extracted words and patterns.

Through a digital interface, the physical hierarchy of archives is *de facto* **rearticulated** in a way or another on the screen. This a problem to be tackled during the digitisation project.

When poorly thought, the conversion of dimension attached to digitisation **can actually worsen the information accessibility**. A physical document can always be found when looked for long enough; on the other hand, if the search engine is deficient, some documents can be fully unaccessible. (Europeana Iceberg ?)

### 2.3. Digitisation as a logistics problem

Any **digitisation project is, in essence, a Logistics problem**. On can loosely define Logistics as the management of the flow of things.

Like in any logistics operation, **standardisation is the key**: similar entities must be organised in similar categories.

The first step in this direction is to access the archives in a standard way. Now, part of this problem is actually solved as the physical archive has most likely already been thought as an optimised interface (as opposed, say, to a family house attic).

**The Library-Machine**

This leads to a concept we could call the **Library-Machine**, in which the circulation of humans (a so called "Front-end") has been thought symmetrically to the circulation of objects (in the "Back-end"). The desired objects are brought to the reader by a **series of machine and human interventions** — with the former taking progressively more importance over the latter (as a side note, this raises the question of having the logic of human organisation being replaced by one deemed optimal by machines).

To track object circulation, one must associate each physical object with a **unique ID**. Each physical object therefore must become a proper document, ready to be manipulated through a standardised process. For example, two specimens of the same book must have two different IDs. In most cases, the ID is the ID of one container (book, box); the documentation level thus must be chosen.

Through standardisation, the digitisation process can be estimated using simple metrics (pages, kilometers, etc.) and a digitization price/page or /km can be established. In many cases, it is impossible to know a priori the number of pages and therefore, the estimation in km is the only option.

### 2.4. Optimisation prospects
#### 2.4.1. Alienation

Alienation is one of the risk of the optimisation process. In a highly-standardised logistical system, human operators, who help the system run, are but a **part of a bigger machine**.

The repetitiveness of the task, as well as a distance with regards to the document understanding, can be problematic (even more so when the content dealt with has such a "humanistic" meaning).

Designing against alienation thus becomes part of the logistics of digitisation processes: working in pairs, manipulating relevant documents, having a chance to mine the archive, are among possible solutions to mitigate the repetitiveness of digitisation.

#### 2.4.2. On-demand digitisation

With **on-demand digitisation**, one can ask for the digitisation of a specifically chosen document. The requested digitisation is then done in a couple of days/weeks. Once the digitisation is done is it downloadable directly form the website.  

In many system, digitisation assets are organised by Tier. Tiers range from very often used data (Tier 0) to data never checked (Tier 3). A physical document can be considered as “not cached” content with a longer retrieving time expected, but which can be brought to a higher-level tier by digitisation.

On-demand digitisation is also a way to reduce the proportion of **efforts put in digitising items that nobody will ever see** (which represent the vast majority), thus improving the investment-to-relevance ratio of the digitisation project. However, an efficient on-demand digitisation process would require complete catalogues of archives, which institutions very rarely have.

#### 2.4.2. Optimising the choice of sources

We've seen that part of the success of the Google Books project was due to an optimal choice of initial sources.

Even if most of digitisation project are done with a specific goal are are tied to a specific documentary fund, we can still ask ourselves how the **choice of documents to digitise can be optimised** in larger scale projects.

The answer to what should be digitised first lies in the balance of some criteria:
- Popularity;
- Fragility;
- Information richness.

An historian would insist on focusing on **rare**, possibly unseen-before, documents. On the other hand, an archive director would probably favour popular and much-demanded but **fragile** items.

From the point of view of a digital humanist, the priority should be given to regular, **standardised** documents, from which information can be **massively extracted** (in the case of the Venice Time Machine: cadasters, directories, tables, etc.)

The case of optimisation for information richness is one of the applications of the **Optimal Experiment Approach** (or Design), whereby **gain (and reinforcement) is evaluated in terms of knowledge gain or uncertainty reduction**, and can be optimised by an **algorithm**.

More conceptually, let's represent the by one space the wealth of documents to digitise. Imagine we now divide it in subspaces, according to some criteria, and estimate how much can be learned from this subspace, and how well.

What we want is to **maximise the learning** of the system, that is to maximise the derivative of the error curve. The priority should be given to subspaces where learning is efficient and where the error quickly decreases; and, on the contrary, poorly-learning systems should not receive too much attention, and resources should be directed to more promising sources of information.

---

## 3. Conclusion
### 3.1. Summary

- Digitisation goes beyond a series of tricks and good practices. It is the **study of optimal actions** in the physical and digital worlds in terms of selection, documentation, acquisition in order to lead to a potential increase in knowledge.

- The progressive change of scale of the practices shows that is should be considered a true branch of information sciences.

- Could/Should the machine help us optimise our patrimonial conservation and exploration strategies?

### 3.2. In the next chapter

In the next chapter we will study how to represent the structure of a document.

---

## Further reading

- Suzanne Briet, Qu’est-ce que la Documentation?  1951

Une étoile est-elle un document? Un galet roulé par un torrent est-il un document? Un animal vivant est-il un document? Non. Mais sont des documents les photographies et les catalogues d’étoiles, les pierres d’un musée de minéralogie, les animaux catalogués et exposés dans un Zoo.

- Alain Jacquesson, Google Livres et le futur des bibliothèques numériques, Editions du Cercle de la Librairie, 2010

- Jean-Noel Jeannerey, Quand Google défie l'Europe: Plaidoyer pour un sursaut, Mille et une nuits, 2007

---

To add somewhere?

## 1. How to plan a digitisation project

Can we digitise 80km of document in 10 years

1) Estimate the number of persons

2) Decide the kind of scanners to be used

3) Estimate the size of the data storage needed

4) Estimate the overall budget

Sampling method and quality control

#### What scanners to use

Various typologies of book scanners

- Sheet-fed scanners can be used if book can be cut to be open
- Book scanners with manual page turning
- Book scanners with automatic page turning

Some project brings the scanners close the collections to be scanned (e.g. First phase of the Venice Time Machine project )

In other cases, the collections are sent to more efficient scanning houses (e.g. Google Books general strategy).


#### Sampling methods

Tbd
