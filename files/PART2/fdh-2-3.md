---
title: 'Foundations in Digital Humanities 2.3'
subtitle: 'Writing Systems'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Writing Systems

#### Theses

1) Many writing systems exist.

2) They get transformed when operationalised by a new technology (Printing press, Digital Computer).

3) Ways of writing handwritten and printed texts change over time.

4) For creating digital representations of these texts one needs to combine powerful digital typography and universal textual representations standards.

This lecture will briefly present the evolution of handwritten and printed texts. The ways to encode this evolution will be detailed in the following lecture.

## 1. Scripts

### 1.1. Defintions
#### 1.1.1. Scripts and Writing Systems

First, let's start with some definitions:

**_Writing_** is the act of recording language in medium more permanent than speech, by means of a script.

By definition, a **_script_** is a set of conventional symbols that can be used to represent in writing one or more languages. Components of a script are characters, or more generally **_graphemes_**.

A **_writing system_** is the use of a script in a particular language. The writing systems defines rules and convention on how to interpret the scripts.

#### 1.1.2. Characters and Glyphs

The graphical representation of a character (ie. grapheme) is called a **_glyph_**.

Beware, however, the relationship between glyph and grapheme is not singular, and the way of writing may depend on the context.

_One character may indeed be represented by different glyphs_: depending on the typeface, the letter case, or the handwriting, the same character can take different representations. In some writing systems, different positions within the word or the sentence call for different glyphs – like is the case for some arabic characters, or for example, with the character sigma (commonly <σ>, but <[ς](https://en.wiktionary.org/wiki/ς#Greek)> when at the end of the word).

Similarly, a glyph may not correspond to a single character (& is a ligature of “e” and “t” and represents “et” or “and”)

In a way, scripts and writing systems formalisations can be thought of in a similar way as Speech2Text and Text2Speech technologies.

### 1.2. Scripts Typologies

We can divide the many scripts that exist or have existed into different categories, according to the value given to their glyphs:

- **Pictographic/Ideographic**: Glyphs are _ideograms_ representing **concepts** (rather than words). Examples include the Aztec writing, or the _Adinkra_ still used in modern Ghana, ..)

- **Logographic**: Glyphs represent **words or morphemes**, which when are read combined to form the word. Examples include: Egyptian, Mayan, or Chinese.

- **Syllabaries** : Glyphs represent **syllables**. For example, Japanese Kana, or Cherokee.

- **Segmental scripts** : Glyphs represent **phonemes**. Some have only consonants (in which case the system belongs to the _abjad_ family, like Hebrew), some combine consonant and vowel in a unique grapheme (the _abugida_ family, e.g. the Brahmic scripts), and finally some are _True Alphabets_ (in which both vowels and consonants have their own grapheme; like in Greek, Latin, or Cyrillic).

All these examples of scripts have their graphemes effectively represented by a series of lines. They are known as **_linear alphabets_**.

But there also exist **non linear alphabets**, which are composed of something other than lines on a surface; for example, Braille, Morse code, or International Maritime Signal Flags.

- **Undeciphered systems** and documents

Among the many systems still to be deciphered today, some could be writing systems:
- Cretan hieroglyphs
- Indus Valley Civilization scripts
- Linear A (Minoan)
- Phaistos Disc

Some manuscript writings are also in undeciphered and unidentified writing systems – the most famous example being the Voynich manuscript. Some of them could be hoaxes.

### 1.3. Operationalisation of writing scripts. Focus: McLuhan and the Typographic Man

_Writing systems evolve over time_. Most importantly, they can be **operationalised** using mechanic or digital technology. This causes profound transformation of their diffusion and usage.

In _The Gutenberg Galaxy_, Marshall McLuhan (1911-1980) argues that the phonetic alphabet and then the printing press have changed the human mind.

With the creation of the movable type, the invention of the “Typographic man” at the Renaissance permits the standardisation and centralisation. For McLuhan, the electronics and the digital announces the a new era, a great mutation, a return to orality.

Each writing system, he argues, has a profound effect cognitive and cultural effect: they exert a **“gravitational effect”** on cognition.  Print technology made possible salient trends in the Western World: individualism, democracy, protestantism, capitalism and nationalism. They are all based on the "segmentation of actions and functions and principle of visual quantification”.

Side note: An interesting parallel is that decipherment techniques are changing mimicking the change in digital techniques; as an example, current attempts at deciphering the Voynich manuscript make use of recent AI advances.

## 2. Handwritten texts

### Evolution of handwritten texts

Reading difficulty changes with time but paradoxically it is not necessary the older documents that are the most difficult to recognised.

The more writing skills get diffuse in the population, the less standardised are the handwritten documents.

The handwriting found in some medieval manuscript is often more regular than modern handwriting. From a machine-vision point-of-view, it is much easier to read an old document than a recent one.

In the Carolingian minuscule, the script used in Charlemangne’s empire and its successor states (800-1200) letters and words are clearly separated.

Caveat: Importance of compairing similar domain documents (adminstrative vs. adminstrative, personal vs. personal, etc.).

### Abbreviations

A problem: Medieval texts are highly “compressed”.

One of the central skills in paleography is understanding abbreviations and expanding them correctly.

Major reference works date from the 19th century:
- Chassant (1845)
- Trice Martin (1892)
- Cappelli (1899)

Limit of the glyph system: other glyphs (for abbreviations) exist beyond the alphabet.

Three systems of abbreviation in the antiquity (only indirect evidence as no Roman manuscript is known as an autograph):
- Tironian notae (system for making quick transcriptions)
- Notae Iuris (abbreviations used by the legal profession)
- Nomina Sacra (abbreviations found in early Christian writings)

Motivation for abbreviations :
- save space or to save time, but not only :
- language-independent communication in a multilingual environment
- the avoidance of using a sacred name
- allegoric, ritualistic, and occult purposes related to alchemical and magical symbols

Examples

Suspension : abbreviating a word by omitting a number of characters at the end

AUG. ‘Augustus’

ib. ‘ibidem’

fq ‘filius quondam’

R.I.P. ‘Requiescat in pace’

D. ‘Dux’ or ‘Dominus’

MSS. ‘Manuscripta’ or ‘Manuscripts’

pp. ‘pages’

Contraction : omitting letters from the middle of the word.

caplo ‘capitulo’

ds ‘deus’

Signs which indicate the presence of an abbreviation

sign ***ꝯ\*** may stand for ‘con-’ and ‘com-’ when in word-initial position

The superscript letters: specific type of abbreviations in which part of the abbreviated word, often the last letter, is written above the line

w_t ‘with’

Special signs include symbols used for common words, monetary units (£ € $), alchemical, astrological, magical and hermetic symbols.


Abbreviations help to limit ambiguity, ie. to homogenise (of different dialects for examples) by using a "least common denominator".

### Handwritten text databases

MNIST and others
Importance of databases for training computer vision.
Current efforts to construct database.

One of the limitation for glyph reading: lack of databases.

## 3. Printed Texts

### The Printing Revolution

Printed texts are noting but uniform in time. In practice they cover a 500y old period.

Printing with woodblocks started in China in the 9th century.

Metal movable-type printing began to be used in Korea, 400y later.

But it is in Europe that printing became a revolution.

Before 1450, all books were written by hand. In 1455 the Gutenberg Bible was printed in Mainz.

Fifty years after, millions of printed books circulated around Europe. Only 500 000 survive of these "incunables" today.

A technical-industrial process born in the middle of the 15th century in a strip of land between France and Germany, a kind of “Silicon Valley” of that time.

The medieval world was changing with urbanisation and growth of mercantile classes. Demographic decline following the Black Death in 1348 and subsequent wars result in a a rise of labour costs and the search for innovation.

Context: The use of paper has driven down book-production costs. Metal was taking over from wood in every technological process. And more importantly, there was a demand for more and more books.

### Typefaces

Seven typefaces were developed in the 15th century. Quickly they settled down to a few specific types. They imitate the hand of scribes.

- Roman
- Gotic
- Batarde
- Greek
- Hebrew
- Glagolitico
- Italic

As most printers had their own sets cuts, there was a huge variety of letter-forms within a typeface style – can be used to track down where the book is coming from.

### Redocumentation of handwritten books

Important moment: printed books are redocumented versions of handwritten books, not new works. Dramatic increase of some ideas, based on the selection. Shaped the cultural landscape for decades if not centuries in Europe. _Who made the selection?_

In the early years of printing the goal was to redocument as quickly and economically as possible handwritten books. The printed books needed to look as close to the manuscripts as possible.

What survives today from 1450-1500? 28,000 editions in 500 000 copies conserved in 4000 public libraries but also in un unknown number of private collections.

The largest majority of them are in Latin (21 329), _the_ language of communication across Europe. Latin is followed by German (3308), Italian (2433), French (1780), Dutch (571), Spanish (437), English (240), and Hebrew (154).

(Figures from Dondi, Printing Revolution)

Most common subjects : Theology (4928), Law (4480), Literature and Classics (4313), Liturgy (2245), Devotional Literature (1893), Moral Literature (1499), Philosophy (1476), Current affairs (1041), Medicine (940), Ecclesiastical History (725), History (678), Bible (337), Natural Philosophy (265), Mathematics (98), Geographia (88), Agriculture and Music (55), Architecture and Engineering (22).

(Figures from Dondi, Printing Revolution)

### Evolution of Typography

Letraset popularised Lorem Ipsum.

The Macintosh introduced a confusion in terms of terminology.

A typeface is the design of lettering that can include variations, such as extra bold, bold, regular, light, italic, condensed, extended, etc.

Each of these variations of the typeface is a font.

But many people use the term “Font” to refer to Typeface

## Spellings

Modern languages are taught in school, well-documented by grammars and dictionaries, which are a relatively new invention (the first widely-accepted dictionaries in Europe only emerged at the end of the 17th Century).

Modern languages have standard orthographies. This makes it possible to correct misspellings.

Large amount of text are available for modern languages. Even for small languages, there are typically large newspaper or administrative corpora to train train text processing techniques.

Historical languages often do not benefit from a standard orthography. A word may be spelled differently by the same author in the same text. Most Text Processing techniques assume that a word is always written in the same way – hence the difficulty of historical language processing.

Spelling variation exist in modern language (e.g. American vs British spellings) but is much rather and well documented.

Spelling is not limited to the spelling of individual words, it also concern punctuation, abbreviations, hyphenation, word separation. The ambiguities in punctuation can often be lifted using standard rules, but those are hard to establish in a pre-standardised stage in a language.

There are many examples of spelling change and rectification in French, Dutch, German, etc.

This is also true for Chinese, Turkish, Korean, Mongolian.

Change occurs diachronically but also synchronically.

Often, most ancient text written in an historical form of the language get redocumented using the new form (sometimes more complex like in French).

Most digital historical texts are not originals but transcriptions. Different types of transcriptions exist

Diplomatic transcription : render every feature of the original text the can be reproduced including page layout, line breaks, original spelling and errors

At the other extreme :

Fully modernised transcription : Spelling and layout is transformed to facilitate reading and dissemination. Scholars may consider this a translation more than a transcription.

Any transcription and redocumentation implies some interpretation and remapping. Therefore in most case the a digital text is the results of complex sequence of redocumentation process.

In general, spelling variations do decrease over time. (cf. Buntinx and Kaplan, 2018).

## Summary

Historical texts are challenging because they use ancient Writing Systems that needs to be redocumented in contemporary forms.

## In the next chapter

We will see how to encode an historical text digitally

## Questions and answers

- Is a music sheet a Script ? No. It is formally a more complex system than most of the system we have discussed as i can encode complex polyphony. All the other scrpits deals with linear encoding. (A special chapter is dedicated to Music systems)
- Is a sign language a Writing System ? No it is kind of oraliy. It cannot be recorded. 
- Is the phonetic alphabet a Writing System ? Yes. 

## Further reading

- Dondi, Printing Revolution

- Richard Sproat, A Computational Theory of Writing Systems

- McLuhan, The Gutenberg Galaxy

- Clarisse Herrenschmidt, 2007, Les trois écritures. Langue, nombre, code, Paris, Gallimard