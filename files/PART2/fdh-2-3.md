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

# FDH-2-3: Writing Systems

#### Core theses explored in this chapter

1) Many writing systems exist.

2) They get transformed when operationalised by a new technology (Printing press, Digital Computer).

3) Ways of writing handwritten and printed texts change over time.

4) In order to create digital representations of these texts, one needs to combine powerful digital typography and universal textual representations standards.

This lecture will briefly present the evolution of handwritten and printed texts. The ways to encode this evolution will be detailed in the following lecture.

#### Contents
1. Scripts
> 1.1. Defintions // 1.2. Script Typologies // 1.3. Operationalisation of writing scripts. Focus: McLuhan and the Typographic Man //
2. Handwritten texts
> 2.1. Evolution of handwritten texts // 2.2. Focus: Medieval abbreviations // 2.3. Handwritten text databases //
3. Printed Texts
> 3.1. The Printing Revolution // 3.2. Redocumentation in the early days of printing: from handwritten to printed books // 3.3. The evolution of Typography //
4. Spellings
> 4.1. The recent standardisation of language rules // 4.2. Linguistic heterogeneity in older texts // 4.3. From an historical text to a modern transcription //
5. Conclusion
> 5.1. Summary // 5.2. In the next chapter //

---
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

### 1.2. Script Typologies

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

----
## 2. Handwritten texts
### 2.1. Evolution of handwritten texts

We now turn our attention to handwritten texts. A first paradox emerges: Reading difficulty changes with time but it is not necessarily the older documents that are the most difficult to recognise.

**The more writing skills get diffuse in the population, the less standardised are the handwritten documents.**

The handwriting found in medieval manuscripts is often more regular than modern handwriting. From a machine-vision point-of-view, it is much easier to read an old document than a recent one.

A clear example is the Carolingian minuscule — which was used in Charlemagne’s empire and its successor states (800-1200): in this script, letters and words are clearly separated and thus very ease to read.

### 2.2. Focus: Medieval abbreviations

When we try to read historical texts, we are quickly faced with a problem: texts can be highly “compressed” by means of **abbreviations**, as is especially true for Medieval works.

Understanding abbreviations and expanding them correctly therefore becomes one of the central skills in paleography, as can be seen in the flourishing of reference works in the 19th century: Chassant's 1845 _Dictionnaire des abréviations latines et françaises ..._, or Cappelli's 1899 _Lexicon Abbreviaturarum Dizionario Di Abbreviature Latine Ed Italiane_.

The possibility of such "compressions" is the limit of the glyph system, whereby other glyphs (the ones used for abbreviations) exist beyond the alphabet.

In the case of Antiquity, three systems of abbreviation are thought to have been used ("thought" as there is only indirect evidence and no Roman manuscript is known):
- **Notae Tironianae**: a system to make quick transcriptions
- **Notae Iuris**: abbreviations used by the legal profession
- **Nomina Sacra**: abbreviations found in early Christian writings

The motivations for abbreviating text are numerous and explain their wide use:
- They **save time or space** (which can be a limited resource, like on a building facade for example).
- They can be a form of **language-independent communication** in a multilingual environment. For example, it not rare to see abbreviations in texts shared among different dialects (where only the last few letters change); in which case, using the "greatest common divisor" helps homogenise the reading and lift ambiguities.
- The avoidance of using a sacred name.
- Or even allegoric, ritualistic, and occult purposes related to alchemical and magical symbols.

#### 2.2.1. Types of abbreviations

**Suspension**: Omitting a number of characters at the end.
- AUG. = 'Augustus'
- ib. = 'ibidem'
- fq = 'filius quondam'
- R.I.P. = 'Requiescat in pace'
- D. = 'Dux' or 'Dominus'
- MSS. = 'Manuscripta' or 'Manuscripts'
- pp. = 'pages'

**Contraction**: Omitting letters from the middle of the word.
- caplo = 'capitulo'
- ds = 'deus'

**New marks** which indicate the presence of an abbreviation, either according to the sign on which they are attached, or independently:
- the sign ***ꝯ\*** may stand for 'con-' and 'com-' when in word-initial position

**Superscript letters**: specific type of abbreviations in which part of the abbreviated word, often the last letter, is written above the line.
- w<sup>t</sup> = 'with'

**Special signs** include symbols used for common words, monetary units (£, €, $), alchemical, astrological, magical and hermetic symbols.

One example: the dedicatory inscription on the frieze of Paris' Collège des Quatres Nations makes extensive use of abbreviations to compensate for the lack of space.
The inscription reads: "IVL.MAZARIN.S.R.E.CARD.BASILICAM.ET.GYMNAS.F.C.A.M.D.C.L.X.I"
which, in Latin, expands to "IVLius MAZARINus Sanctœ Romanœ Ecclesiœ CARDinalis BASILICAM ET GYMNASium Faciemdum Curavit Anno MDCLXI" ("Jules Mazarin, Cardinal of the Holy Roman Church, had these chapel and college built in 1661".)

### 2.3. Handwritten text databases

The algorithmic methods to read handwritten texts will be presented in a later lecture. Let us simply mention now the importance of having various databases in the training of computer vision. Some are well-known and established like the Modified National Institute of Standards and Technology databse (MNIST), which offers tens of thousands of training and testing images.

In addition to that, current efforts to construct more databases (including in hitherto poorly represented languages) are underway.

---
## 3. Printed Texts

### 3.1. The Printing Revolution

Printed texts are nothing but uniform in time; this naturally comes from its rich 500 years history.

Proto-printing emerged in 9th Century China with the invention of moveable woodblocks. Their metallic version began to be used 400 years later in Korea.

But **it is in Europe that printing became a revolution**, the start of which is marked by the printing of the Gutenberg Bible in 1455. Fifty years after, millions of printed books circulated around Europe. Only 500,000 survive of these "incunabula" today.

The centre of that new technical-industrial process was Mainz, a city located on a strip of land between France and German – a sort of "Silicon Valley" of that time.

_But what were the conditions that made possible this booming "market of knowledge"?_

The medieval world was changing with urbanisation and growth of mercantile classes. Demographic decline following the Black Death in 1348 and subsequent wars result in a a rise of labour costs and the search for innovation. The use of paper has driven down book-production costs. Metal was taking over from wood in every technological process. And more importantly, there was a demand for more and more books.

### 3.2. Redocumentation in the early days of printing: from handwritten to printed books

It is important to understand that at this point, most printed books were redocumented versions of handwritten books, not new works. The heart of the Printing Revolution was **more in making ideas accessible than in these ideas themselves**. This democratisation of knowledge lead to the dramatic increase in popularity of some ideas, which in turn shaped the cultural landscape for decades if not centuries in Europe. This of course prompts the question of _how (or by whom) the choice of diffusing some ideas was made?_ But this matter is likely out of the scope of this course.

In the early years of printing, the goal was to redocument as quickly and economically as possible handwritten books. The printed books needed to look as close to the manuscripts as possible, including the typographical reproduction of illustrations.

**What survives today from 1450-1500?**

_(The given figures are given from Dondi, Printing Revolution)_

28,000 editions in 500,000 copies are conserved in 4000 public libraries but also in an unknown number of private collections.

The largest majority of them are in Latin (21,329), _the_ language of communication across Europe. Latin is then followed by:
- German (3,308)
- Italian (2,433)
- French (1,780)
- Dutch (571)
- Spanish (437)
- English (240),
- Hebrew (154).

The subjects of these incunabula are divided as follows:
- Theology (4,928)
- Law (4,480)
- Literature and Classics (4,313)
- Liturgy (2,245)
- Devotional Literature (1,893)
- Moral Literature (1,499)
- Philosophy (1,476)
- Current affairs (1,041)
- Medicine (940)
- Ecclesiastical History (725)
- History (678)
- Bible (337)
- Natural Philosophy (265)
- Mathematics (98)
- Geography (88)
- Agriculture and Music (55)
- Architecture and Engineering (22).



### 3.3. The evolution of Typography

Let us now take a small detour to typography.

Seven typefaces were developed in the 15th century. They imitate the handwriting style of scribes.
- Roman
- Gotic
- Batarde
- Greek
- Hebrew
- Glagolitico
- Italic

As most printers had their own sets cuts, there was a huge variety of letter-forms within a typeface style – as a side note, these specificities can be used to track down where the book is coming from.

A few centuries later, the Macintosh reintroduces a very historically accurate approach to typography in the digital world. However, it also introduced a confusion in terms of terminology.

A typeface is the design of lettering that can include variations, such as extra bold, bold, regular, light, italic, condensed, extended, etc. Each of these variations of the typeface is a font. Many people mistakenly use the term “Font” to refer to "Typeface".

---
## 4. Spellings

### 4.1. The recent standardisation of language rules
Modern languages, such as taught in school, are well-documented by grammars and dictionaries, which are a relatively new invention (the first widely-accepted dictionaries in Europe only emerged at the end of the 17th Century).

**Modern languages have standard orthographies**. This makes it possible to correct misspellings. Furthermore, large amount of text are available for modern languages. Even for smaller dialects, there are typically large newspaper or administrative corpora to train text processing techniques.

### 4.2. Linguistic heterogeneity in older texts
Historical languages, on the other end, often **do not benefit from a standard orthography**, and it is not rare to see regional variations flourish. In some cases, a word may be spelt differently by the same author in the same text. However, most text processing techniques assume that a word is always written in the same way – hence the difficulty of historical language processing.

Spelling variation exist in modern language (e.g. American vs British spellings) but is much sparser and better documented.

Furthermore, spelling is not limited to the writing of individual words, it **also concern punctuation, abbreviations, hyphenation, word separation**. The ambiguities in punctuation can often be lifted using standard rules, but those are hard to establish in a pre-standardised stage in a language.

There are many examples of spelling changes and rectifications in French, Dutch, German, etc. This is also true for Chinese, Turkish, Korean, Mongolian. Change occurs diachronically but also synchronically In general, spelling variations do decrease over time. (cf. Buntinx and Kaplan, 2018).

### 4.3. From an historical text to a modern transcription
Often, most ancient texts written in an historical form of the language get redocumented using the new form (sometimes adding complexity, like in French).

As such, most digital historical texts are not originals but transcriptions. When faced with an old text, different types of transcriptions are possible:

- A so-called **diplomatic transcription**, whereby every feature of the original text that can be reproduced is rendered, including page layout, line breaks, original spelling and errors.

- At the other extreme lies a **fully modernised transcription**. Spelling and layout are transformed to facilitate reading and dissemination. However, scholars may consider this a translation more than a transcription.

Any transcription and redocumentation implies some interpretation and remapping. Therefore, in most cases, the digital text is the result of a complex sequence of redocumentation processes which need, as always, to be properly gauged.

---
## 5. Conclusion
### 5.1. Summary
Historical texts are challenging because they use ancient writing systems that needs to be redocumented in contemporary forms.

### 5.2. In the next chapter
We will see how to encode an historical text digitally.

---
## Questions and answers

- **Is a music sheet a Script?** No. It is formally a more complex system than most of the system we have discussed as i can encode complex polyphony. All the other scrpits deals with linear encoding. (A special chapter is dedicated to Music systems)
- **Is the phonetic alphabet a Writing System?** Yes.
- **Is a sign language a Writing System?** No it is a kind of orality. It cannot be recorded.
- **When we contrast the reading difficulty through time, shouldn't we always compare documents with similar "functions" (administrative vs. administrative, personal vs. personal, etc)?** Yes, it is necessary, as the degree of standardisation within the writing partly comes from its "function". (Although the point we make in the lecture is more conceptual than based on rigorous historical examples.)

## Further reading

- Dondi, Printing Revolution

- Richard Sproat, A Computational Theory of Writing Systems

- Knuth, Digital Typography

- McLuhan, The Gutenberg Galaxy

- Norm (Swiss Font creators) on typologies and Writing Systems

- Clarisse Herrenschmidt, 2007, Les trois écritures. Langue, nombre, code, Paris, Gallimard

- Simon Horobib, How English became English

- Albert Derolez, The Paleography of Gothic Manuscript Book. Cambridge

  
