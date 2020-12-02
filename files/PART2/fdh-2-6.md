---
title: 'Foundations in Digital Humanities 2.6'
subtitle: 'Text Understanding'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# FDH-2-6: Text Understanding

#### Theses

1) Machines help us studying more texts and digging the “great unread” (the set of unread texts, far away from canonical texts).

2) Most of the Distant Reading approach stay on the surface of text using only text processing techniques.

3) But progresses in Text Understanding may help reading more text in a deeper manner.

## 1. Close, Surface, Distant, and Machine Reading

Reading is traditionally defined as negotiating 'your' way through a text. As such, the act of reading can be thought of as "walking the book". During their "walk", the reader interprets sequences of words to develop a coherent situation model (a self-coherent fictional space) — the minimal requirement for a successful comprehension of text.

(This section is based on Kestemont, M. and L. Herman. “Can Machines Read (Literature).” (2019).)

### 1.1. Close reading

***Close reading*** is about paying attention to the formal details of a literary text, diving profoundly into the book (in an almost religious fervour). Most scholars in Humanities agree that this is the academic way.

Close reading was developed and popularized in the 1940s and 50s by the “New Critics”, pointing to the work of I.A. Richards and William Empson as sources of inspiration. They advocated a respectful and penetrating attitude, which they viewed as needed to understand a text.

Close reading can only be taught by example because of its relative lack of discovery procedures that might help transfer reading strategies from one text to another. Nevertheless, close reading seems to be the most important teachable skill in courses on literature.

It also the mark of a “tribe” and common values, as it indicates positive attitude towards the literariness of a text, the quest for finding a meaning that is not immediately apparent, by a full immersion in the depth of the text.

### 1.2. Surface reading

First attacks on close reading did not come from Computer Science, but instead by people within Humanities (notably in gender studies, or cultural studies), who criticised the ideology behind close reading.

***Surface reading*** corresponds to methods of reading literature that no longer look for the hidden meaning of a text. It concentrates on “what is evident, perceptible, apprehensible in texts” and, as such, (supposedly) free from interpretative projections.

*Best, Stephen and Sharon Marcus. 2009. “Surface Reading: An Introduction.” In “The Way We Read Now”. ed. Stephen Best and Sharon Marcus, special issue, Representations 108 (1): 1-21.*

The ‘Surface’ in question is the location of patterns that exists within and across texts.

*“We want to reclaim from this tradition the accent on immersion in texts […], for we understand that attentiveness to the artwork as itself a kind of freedom”*

### 1.3. Distant reading

Distant Reading’ is a term introduced by Franco Moretti in 2000 in a series of essays in the New Left Review, reprinted in 2013 in a book called _Distant Reading_.

*Moretti, Franco. 2013. Distant Reading. London: Verso.*

One of the objective of Distant Reading is to go beyond the obligatory canon of well-known (English-language) authors — the canon —, extending the analysis to the “great unread” (Margaret Cohen). To do this, “simply reading more” is unfeasible; and a new kind of reading is needed.

*Cohen, Margaret. 1999. The Sentimental Education of the Novel. Princeton: Princeton University Press.*

Moretti argues that **the more we read, the shallower our reading must become**: ‘the ambition is now directly proportional to the distance from the text: the more ambitious the project, the greater must the distance be’.

While Close Reading can be viewed as “a theological exercise and the very solemn treatment of very few texts taken very seriously”, Distance Reading on the other hand is a more inclusive, let alone exhaustive, study of world literature.

*Moretti, Franco. 2000. “Conjectures on World Literature.” New Left Review 1 (Jan-Febr): 54-68*

Distant Reading is defined negatively, implying the absence of a ‘a single direct textual reading’. Moretti in essence says that ***"to read more, one should not read at all"***.

In practice, Distant Reading has rapidly become an umbrella term for all forms of computational text analysis of large collections of texts. It is surprising to observe that computers or digital methods are not even once explicitly mentioned by Moretti.

For him, Distant Reading initially meant reading on the basis of other readings, and not necessarily, let alone exclusively, reading via computer applications. Moretti argues that one of the strength of Distant Reading is the promise of falsifiable conjectures (in the Popper’s sense).

#### 1.3.1. Operationalizing

Moretti described the concept of ***'operationalizing'*** as like "building a bridge from concepts to measurement, and then to the world", stating it has an absolutely central place in this new field of computational criticism, that includes distant reading (Moretti, F. (2013). "'Operationalizing': Or, the Function of Measurement in Literary Theory". New Left Review.).

Operationalizing consists in taking a concept and transforming it into a series of operations.

This opens for a theory-driven, data-rich research program for studying domains based on the large text corpus. In that sense, the computational process is not fast. It is, on the contrary, a slow explication and operationalisation of hypotheses and conjectures.

### 1.4. Machine reading

Although originally not intended as such, the current usage of the term Distant Reading entails a form of Machine Reading, since readers outsource a significant part of the traditional reading process to a machine.

Human interpretation happens at the level of the output of a computational reading process, i.e. the simplified model of a text corpus that it has yielded.

Distant Reading through Machine reading is currently limited by the performance of Text Analysis pipelines.

Whereas surface readers deliberately choose to stick to a text’s surface, distant readers are currently still practically hindered by the lack of a suitable technology to produce deeper readings of texts, even if they wanted to dig beneath a text’s symptomatic surface.

There is a paradox between the fact that Reading is universally recognised **as complex and individual interpretative process** and the ambition of designing more and more complex Reading Machines, acting maybe as a Universal Reader. Distant reading is currently unsituated and uncontextualized.

Distant Reading is a form of artificial reading (i.e. reading performed by an artificially intelligent agent). With progress of Natural Language Processing, Distant Reading / Machine Reading can dig deeper under the surface of texts.

---

## 2. Information extraction

Text Understanding aims at extracting information from texts.

(Section inspired by : Ehrmann, Romanello, Clematide NE processing in Digital Humanities, Utrecht, July 2019)

Example :

How can one correctly identify and categorise information fragments into a coherent information space?


**Unstructured Text**

_“On the invitation of the Festival de Cannes, the Italian actress Monica Belucci has agreed to play the role of Mistress of the opening and Closing Ceremonies of the 70th Festival de Cannes to be held from 17 to 28 May 2017, under the presidency of Spanish filmmaker Pedro Almodovar.”_

**Identify information fragments**

- PERSON: Monica Belluci, Pedro Almodovar
- ORGANIZATION: Festival de Cannes
- TIME-EXPR: from 17 to 28 May 2017
- EVENT: 70th Festival de Cannes

**Linking with knowledge bases**

- Monica Belluci: Is a reference to http://dbpedia.org/page/Monica_Bellucci
- 70th Festival de Cannes: Is an instance of: http://en.wikipedia.org/wiki/Cannes_Film_Festival

**Extracting and normalising information**

- Going from "17 to 28 May 2017" to _[17-05-2017, 28-05-2017]_

**Relation Extraction**

- 70th Festival de Cannes, **tookPlace**, [17-05-2017, 28-05-2017]

Application includes:

- Literature : Studying character networks
- History : Extracting historical events corresponding network of actors.

    Example 1. Alex Woloch's book ("The one and the Many, Minor characters and the Space in the Novel", 2003) imagines the novel as a space, in which all the characters would be in conflict to be in the front row. Woloch shows that this rivalry is the subject of several 19th century novels.

    Example 2. Analysing character networks in Rousseau's confessions can be operationalized.

---

## 3. History of Machine Reading

The history of Machine Reading is one of ups and down. Text Understanding started in the 1980s with an over-ambitious project facing technical and theoretical difficulties:
- low coverage of grammars
- too many unsolved ambiguities
- difficulties to collect, represent, and manipulate knowledge

In the 1990s, ambitions were tamed and efforts focused on information extraction (entities, events, relations) based on models defined in advance. The Message Understanding Conference (MUC) played a pivotal role in the advances in the field. Initiated by the U.S. Naval Research and Development division and financed by the DARPA (Defense Advanced Research Project Agency), it organised 7 evaluation campaigns between 1987 and 1998.

It is in these campaigns that the concept of ***Named Entities*** (NE) appeared. NEs quickly gained prominence and became one of the central hubs in automated text analysis systems.

- **1987 (MUC-1)**. First conference, focusing on military reports on fleet operations in telegram style, but with no clear task.

- **1989 (MUC-2)**. Definition of predefined templates which had to be filled (10 slots); definition of evaluation measures (adoption of the well-known **Precision and Recall**).

- **1991 (MUC-3)**. Template with 18 slots: broadcast news on terrorist events in Central and South America.

- **1992 (MUC-4)**. Idem with 24 slots.

- **1993 (MUC-5)**. Very complex, new domain, 2 languages, 11 templates organised hierarchically with 48 slots.

- **1995 (MUC-6)**. Frame reformulation towards task independent components and technologies. Definition of "**named entity**" sub-task.

- **1997 (MUC-7)**. Continuation.

Since 2009, a follow-up effort, the _Text Analysis Conference Knowledge Base Population_ (TAC-KBP) has engaged in discovering information about NEs as found in a large corpus and incorporate this information into a knowledge base.

Given an entity, one should find its attributes; e.g. for a PERS, these would include:
- names: other names of the person (alias, fake names, stage name)
- functions and activities: jobs, occupations, etc.
- dates (or age): birth, death, different life events, age ;
- locations: places related to life events (birth, death, jobs)
- related persons: spouse, children, family members
- other information: alma mater, visited countries

In a way, this is a return to the initial ambition of Text Understanding. But the task remains very complex despite significant progress.

Mihai Surdeanu and Heng Ji, Overview of the english slot filling track at the tac2014 knowledge base population evaluation, Proc. Text Analysis Conference (TAC2014), 2014.

---

## 4. Named Entities as pivot points

When the aforementioned predefined templates were first used, it was discovered that some elements were easier to identify than others: named entities, corresponding to persons, places, organisations, etc. Their discovery was also made easier by the creation of the first databases. Following that, the field reorganised itself around the detection of these Named Entities, which were to act as pivot points, from which relations and attributes of entities could be more easily inferred.

Named entities are referential units which underly the semantics of texts. Given an application model and a corpus, a named entity is a **linguistic expression that refers to a unique entity** of the model autonomously in the corpus.

“Elements of interest" are generally of type Person, Organisation, Location (Universal Triad).

- **Proper nouns** refer to individuals:
  - naming of an individual (Felix) vs. naming of a class (cat)
  - uniqueness: an individual considered as unique within a category of entities
  - identity: an individual considered as a recognizable whole at all time.


- **Definite descriptions** can also point to individual people or objects (presupposing their existence and uniqueness) : the president of the Republic, the father of Elisabeth II, James Bond's car.

Standing in between linguistic categories, Named Entities are ***‘More than proper names, but less than definite descriptions’***, and autonomously reference a unique entity.

Named Entities serve different purposes:

1. **Recognition**: Detecting, spotting named entities in textual streams: one delimitates NEs ’boundaries’ in texts).

2. **Classification**: Categorizing detected segments according to pre-defined semantic categories: one assigns a type.

3. **Disambiguation/linking**: Linking entity mentions to a unique reference: one determines the reference.

4. **Relation extraction**: Discovering relations between NEs: e.g.father-of, born-in, alma mater.

In all those tasks, disambiguation is key:
- _Java_ can refer to an island, a coffee, a programming language;
- _Orange_ can refer to a city, a company, a fruit, a color;
- _G. Bush_ can be the father or the son;
- _Berkeley_ can be a university, a city, a philosopher;
- _Paris_ has more than 50 different pages in Wikipedia...

The Stanford NER project is one of the leading efforts in this entity disambiguation task.

---

## 5. Resources

### 5.1. Typologies

- Typologies ACE

- Quaero typology (8 main categories)

  • Person: individual person, group of persons;
  • Location: administrative location, physical location, facilities, oronyms, address;
  • Organization: administration, service;
  • Time: absolute and relative date, absolute and relative hour;
  • Amount;
  • Product: manufactured object, transportation route, financial products, doctrine, law, software, art, media, award;
  • Function: individual function, collectivity of functions

### 5.2. Gazetters

Objective: provide information relating to entities which may be used by automatic systems for the purposes of recognition, classification and disambiguation.

2 types of information:

• lexical, on lexical units composing entities

• encyclopaedic, on entity referents

Significant evolution of these resources since the 90s:

\- complexification: basic ‘gazetteers’ -> bases encoding of more and more information.

\- less central: essential for the recognition and classification of NEs up to now, moving to the background with deep learning.

Geonames :

• toponyms

• 7 millions entities and 10 millions lexical entries (variants)

• properties: coordinates, population, postal code, etc.

• assignment of an URI to each entity

• 9 main types (divided into 645 sub-types)

JRCnames :

 a ‘by-product’ of a media monitoring system: 7000 sources, 300k articles per day, 70 languages, among which 21 with NE processing

• ca. 340,000 unique entities (pers et org)

• 1,7 million name variants (lexicalisations) in 170 languages

• 32 millions relations (cross-lingual)

• up to 400 variants for one entity

### 5.3. Knowledge bases

- Wikipedia (initiated in 2001) : useful for extracting and integrating NE lexicons. semi-automatic constitution of annotated corpora, acquisition of relations between entities

- DBpedia (RDF equivalent of Wikipedia)

- YAGO (Wikipedia, WordNet, with spatial and temporal info)

- BabelNet

- Wikidata

- OpenCyc (free part of Cyc), information about ’common sense’. Douglas Lenat began the project in July 1984. Long-term artificial intelligence project that aims to assemble a comprehensive ontology and knowledge base that spans the basic concepts and rules about how the world works. Hoping to capture common sense knowledge, Cyc focuses on implicit knowledge that other AI platforms may take for granted. The objective of the Cyc project was to codify, in machine-usable form, the millions of pieces of knowledge that compose human common sense. Cyc's ontology grew to about 100,000 terms during the first decade of the project, to 1994, and as of 2017 contained about 1,500,000 terms. The Cyc knowledge base of general common-sense rules and assertions involving those ontological terms was largely created by hand axiom-writing; it grew to about 1 million in 1994, and as of 2017 is about 24.5 million and has taken well over 1,000 person-years of effort to construct.

### 5.4. Large-scale Projects

Open information extraction (OIE) is the task of generating a structured, machine-readable representation of the information in text, usually in the form of triples or n-ary propositions.

A proposition can be understood as truth-bearer, a textual expression of a potential fact represented in an amenable structure for computers

Each texts produces a set of potential facts and relations. This is a Fiction Space that can be integrated with other extraction.  

**Never Ending Language Learning (NELL)**

A semantic machine learning system developed by a research team at Carnegie Mellon University.

Goal : develop means of answering questions posed by users in natural language with no human intervention in the process

---

# 6. Conclusion
## 6.1. Summary

Algorithms can dig under the surface of texts to extract information. They extract structured fictional spaces out of each texts. These fictional spaces can be compared or integrated into larger wholes.

## 6.2. In the next chapter

We will start to study pipelines adapted to Images. Some argue that images can be reduced to text, and therefore the same pipelines can be used. We'll discuss that.

## Further reading

- Moretti, Franco. 2000. “Conjectures on World Literature.” New Left Review 1 (Jan-Febr): 54-68

- Moretti, Franco. 2013. Distant Reading. London: Verso.

- Kestermont / Herman Can Machine Read (Litterature) ?

- Alex Woloch's book (/The one and the Many, Minor characters and the Space in the Novel/, 2003),  

- Never Ending Language Learning (NELL)

- Umberto Eco on Reading Machine, or other.

(Oxford Handbook of Reading)


## To be developed

- Narrative as virtual reality.
- Fictional spaces and modelling of parralel worlds
  - Pierre Bayard, il existe d'autres mondes, Les editions de Minuit
  - The fabrics of reality
  - Other books on alternative reality-
