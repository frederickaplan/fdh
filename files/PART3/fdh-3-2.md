---
title: 'Foundations in Digital Humanities 3.2'
subtitle: 'Universal ontologies'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Universal ontologies

## Theses

1) Some ontologies aim at being universal. 

2) They are tried to solve hard problems like the modelling of time, space, events and relations

## Examples

### Collective ontologies

Universality by incremental consensus. 

Wikidata : 

- A collaboratively edited multilingual knowledge graph launched in 2012
- Each item is allocated a unique, persistent identifier, a positive integer prefixed with the upper-case letter Q, known as a “QID".
- Statements are how any information known about an item is recorded in Wikidata. Formally, they consist of key-value pairs, which match a property (such as "author", or "publication date") with one or more entity values (such as "Sir Arthur Conan Doyle" or "1902").
- A property describes the data value of a statement and can be thought of as a category of data, for example color (P462) for the data value blue (Q1088)
- The most used property is instance of (P31), that is used on more than 53,000,000 item pages.
- Properties may also define more complex rules about their intended usage, termed constraints. For example, the capital (P36) property includes a "single value constraint", reflecting the reality that (typically) territories have only one capital city. Constraints are treated as testing alerts and hints, rather than inviolable rules.

(subject predicate object)

⇔ {subject, statements, value} 

Wikidata has a SPARQL endpoint. 

### Document ontologies

Open Annotation (already seen in past courses)

### Social network ontologies

FOAF (Friend of a friend) is a simple RDF ontology describing persons, their activities and their relations to other people and objects.

## Time

What are the possible relations between two time intervals ?

What is the definition of a calendar ?

What is the definition of a clock ?

### Logical relations in time

W3C Time Ontology based on an early work by Allen (1984)

Towards a general theory of action and time. Artificial Intelligence 23, pp. 123-154.. J.F. Allen. 1984. URL: 

[http://dx.doi.org/10.1016/0004-3702%2884%2990008-0](http://dx.doi.org/10.1016/0004-3702(84)90008-0)

\- The basic structure of the ontology is based on an algebra of binary relations on intervals

“The ontology starts with a class :TemporalEntity with properties :hasBeginning and :hasEnd that link to the temporal instants that define its limits, and :hasTemporalDuration to describe its extent. 

There are two subclasses: :Interval and :Instant, and they are the only two subclasses of :TemporalEntity. Intervals are, intuitively, things with extent. 

Instants are, intuitively, point-like in that they have no interior points, but it is generally safe to think of an instant as an interval with zero length, where the beginning and end are the same.”

Relations between intervals are the critical logic provided by Allen's analysis, and implemented in the ontology. This leads to thirteen elementary relations that support unambiguous expression of all possible relations between temporal entities, which allows the computation of any relative position or sequence.

### Temporal reference systems, clocks, calendars

#### Clocks

> Definition: A clock is a regularly repeating physical event ('tick') and a counting mechanism for the 'ticks'. These counts may be used to logically relate two events and to calculate a duration between the events.

In scientific and technical applications, Julian date counts the number of days since the beginning of 4713 BCE, and Loran-C, Unix and GPS time are based on seconds counted from a specified origin in 1958, 1970 and 1980, respectively, with GPS time represented using a pair of numbers for week number plus seconds into week. 

Do you know any other clocks ?

**Geophysic : UT (Universal time)**

Universal time is a time based on a definition of the second resulting from a division of the average time of the earth's rotation. A day always has the same number of seconds, but the definition of the second varies over time based on the earth's kinematics. This time is defined to correspond to the apparent days due to the rotation of the Earth on itself and around the Sun.

**Absolute : IAT (International Atomic Time)**

International Atomic Time is calculated on the basis of a weighted average of the times given by 500 atomic clocks distributed in 70 laboratories.

As a consequence, International Atomic Time is progressively decoupled from Universal Time, corresponding less and less to the apparent day defined by the Earth's kinematics.

**Absolute coordinated : UTC (Universal coordinated time)**

Like AIT, Coordinated Universal Time is an absolute frame of reference based on the modern definition of the second. It also gives the number of seconds elapsed from a defined origin. Both TAI and UTC are incremented on the basis of the definition of the second.

UTC differs from AIT by an integer number of seconds: 10 seconds of initial offset + number of leap seconds added. On January 1, 2016, the difference between TAI and UTC was 36 seconds.

The leap seconds have the function of artificially "slowing down" UTC so that it never differs from UT by more than one second. UTC is thus constrained to correspond, at best, to the apparent day.

#### Calendars

> Definition : A *calendar* is a set of algorithms that enables clock counts to be converted into practical everyday dates and times related to the movement of astronomical bodies (day, month, year).

- Julian calendar was used throughout Europe until the 16th century, and is still used for computing key dates in some orthodox Christian communities. 
- Lunisolar (e.g. Hebrew) and lunar (e.g. Islamic) calendars are currently in use in some communities, and many similar have been used historically. 
- Ancient Chinese calendars as well as the French revolutionary calendar used 10-day weeks.

#### Case study : French revolutionary calendar

- Retroactively adapted on Sept 22, 1792 lasted until 1805
- Ten days formed a week. Primdi, Duodi, Tridi, … Decadi. Agricultural dedication replaces the Saints Day.
- Three weeks formed a month
- Twelve months formed a year, with names influenced by the weather (Pluviose - Rain, Ventose - Wind, Brumaire - Fog)
- Five patriotic days replaced the new year, les jours sans culottes. Each day dedicated to a civic quality : Genius, Rewards, Opinon, Virtue, Labour

As astronomically based calendars try to fit inconvenient durations into a usable regular system of counting cycles, 'intercalations' are often used to re-align the calendar's repeating patterns with astronomical events. 

These intercalations may be of different durations depending on the calendar, such as leap seconds, leap days, or even a group of days. Leap days are explicit and leap seconds implicit in the Gregorian calendar.

#### Ordinal temporal reference system

> Definition : An ordinal temporal reference system is a set of ordered intervals (e.g. named dynasties, geological periods, geomagnetic reversals, tree rings) that can be used as simple form of temporal reference system supporting logical reasoning,

- Archaeological and geological applications use chronometric scales based on years counted backwards from ‘the present’ (defined as 1950 for radiocarbon dating) or using named periods associated with specified correlation markers
- Dynastic calendars (counting years within eras defined by the reign of a monarch or dynasty) were used in many cultures.

#### Temporal coordinate 

For many purposes it is convenient to make temporal calculations in terms of clock durations that exceed everyday units such as days, weeks, months and years, using a representation of temporal position in a temporal coordinate system or temporal coordinate reference system i.e. on a number line with a specified origin, such as Julian date, or Unix time. This may be converted to calendar units when necessary for human consumption.

## Events

CIDOC-CRM is an ontology for Cultural Heritage

\- About 20 year of work

\- An ISO standard 21127

\- 100+ schema. Very stable 

\- CIDOC-CRM is a tentative to formalise an underlying semantics common to many classifications. It includes very interesting ideas. 

\- In CIDOC-CRM, the modelling is event-centric

\- The underlying idea is to model change, not state. Therefore, temporal entities play a central role. 

\- Instead of coding the birthdate of an actor, it is better to code the event of its birth

\- This is also more in line with the historical recovery/decomposition approach. 

#### Event Constraints

\- The participation of presence of several non-temporal entities in a an event e1 allows to conclude that the have been in hte same time-interval and space, even without knowledge of the particular time and space

\- They must have existed at that time . They have not been somewhere else at that time (with electronic communication, the space volume in which events occur can become very large)

\- The events e0i of creation of each participant I have happened before or at the time of e1. The events e2i of destruction (or vanishing) of each participant have happened after or at time of e1. 

\- The property P11 “had participants” denotes active or passive involvement of Actors, whereas P2 “occurred in the presence of” ranges from objects just being there (e.g. desk where a treaty was signed)

\- The properties P92 “brought into existence”, P93 "took out of existence” are limiting the existence pf things have a persistent existence. 

## Places

How can Places be generally characterised (remember course on Maps)

Places are where events happen. 

In France, in Athens, 39N 124E.

Points given by spatial coordinate are typically understood as the center of wider, extended areas 

On mount St Helens. At the Rhine river.

On Queen Elizabeth (the ship). In my suitcase. At home

Following CIDOC-CRM, geometric areas (E53 Place) can only be defined to larger objects, including the surface of the earth

Those “places” in turn may be located at different times at different places (relative to a larger object)

The cultural interest is in relation to other things and not to an abstract absolute space. Absolute coordinate make no sense when the reference object move. 

 As historical information is incomplete and sparse, and many reference object move, normalisation of place to absolute coordinates should not replace the primary information, which is typically relative. 

(Link with other part on Place / Concrete Shape, etc)

## Influence

\- Another problematic issue is the notion of influence. It is difficult to develop a systematic understanding of the different forms of influence and their mutual relation. 

\- Some are more physical, like using a mould or a tool. The influence of a mould on a produced object is string an can obten be verified on the objects afterwards (see definition of physical connection and physical closure)

\- The influence of a hammer is less specific. 

\- Similarily, making a copy of a painting has a strong influence on the product, copying the idea of painting, a weak one. The latter is moe an intellectual influence that a physical one. The copied objets do not need to be present. 

\- If a strong influence existed, a temporal sequence can be deduced (history recovery problem)

## General principles

> **The property-event equivalence** 
>
> Any property of an actor can be modelled as a past event in which this actor participated. 

Instead of coding the birthdate of an actor, it is possible and better to code the event of its birth. 

It a simpler and more easily extandable representation. 

> **The Time Interval principle** 
>
> Any Time indication is a Time interval

Do not code date, always code Time Intervals. This is much more flexible and permits to detect inconsistencies. 

> **The Place Relativity principle**
>
> Places are always defined relatively to large places

Code places in a relative manner and not an absolute manner. The cultural interest of place is in the relation to other things and not in respect to an abstract absolute space.  

## Summary

A lot of work has been done in ontologies. Extracted knowledge is ready to be processed. But what can we do when data is coded in this manner ?

## In the next chapter

We will look at constraints, rule systems, solvers, simulations and parralel worlds. 

## Further Reading

Towards a general theory of action and time. Artificial Intelligence 23, pp. 123-154.](http://dx.doi.org/10.1016/0004-3702(84)90008-0). J.F. Allen. 1984. URL: [http://dx.doi.org/10.1016/0004-3702%2884%2990008-0](http://dx.doi.org/10.1016/0004-3702(84)90008-0)

[Actions and events in interval temporal logic In: Spatial and Temporal Reasoning. O. Stock, ed., Kluwer, Dordrecht, Netherlands, pp. 205-245.](http://dx.doi.org/10.1007/978-0-585-28322-7_7). J.F. Allen; G. Ferguson. 1997. URL: http://dx.doi.org/10.1007/978-0-585-28322-7_7

[A formal model for the geologic time scale and global stratotype section and point, compatible with geospatial information transfer standards. Geosphere 1 119. ](http://dx.doi.org/10.1130/GES00022.1). S.J.D. Cox; S.M. Richard. 2005. URL: http://dx.doi.org/10.1130/GES00022.1

[A geologic timescale ontology and service. Earth Sci. Informatics.. 8 5–19. ](http://doi.org/10.1007/s12145-014-0170-6). S.J.D. Cox; S.M. Richard. 2014. URL: http://doi.org/10.1007/s12145-014-0170-6

[Time Ontology Extended for Non-Gregorian Calendar Applications. Semantic Web Journal 7, pp. 201-209](http://dx.doi.org/10.3233/SW-150187). S.J.D. Cox. 2015. URL: http://dx.doi.org/10.3233/SW-150187

CIDOC-CRM Doc

