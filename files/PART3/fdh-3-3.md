---
title: 'Foundations in Digital Humanities 3.3'
subtitle: 'Rule systems, simulations and parallel worlds'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Rule systems, simulations and parallel worlds

## Theses

1) History can be considered a giant Sudoku

2) History can be considered a giant Simulation

## Constraint problem solving

### Why History can be considered a constraint problem solving. 

Example of Venice and the catastici. 

### Solving Sudokus

#### An example in Prolog

A few line of Prolog permits to solve a Sudoku problem 

1) Create a constraint stating that the numbers in all line must be different, the number in all columns must be different, the numbers in each square must be different.

2) Ask prolog to find one (or more ) solutions compatible with the constraints. 

You just have to describe the problem to have it solved !

\- Prolog is a logic programming language created in 1972

\- Prolog has its roots in first-order logic, a formal logic.

\- Prolog is Turing-complete

\- Prolog is intended primarily as a declarative programming language: the program logic is expressed in terms of relations, represented as facts and rules. 

\- A computation is initiated by running a query over these relations

Example of a Prolog program

mother_child(trude, sally).

father_child(tom, sally).

father_child(tom, erica).

father_child(mike, tom).

sibling(X, Y)   :- parent_child(Z, X), parent_child(Z, Y).

parent_child(X, Y) :- father_child(X, Y).

parent_child(X, Y) :- mother_child(X, Y).



?- sibling(sally, erica).

 Yes

#### Backtracking

Backtracking is an example of Brute Force algorithm

\- The backtracking algorithm enumerates a set of partial candidates that, in principle, could be completed in various ways to give all the possible solutions to the given problem. 

\- The completion is done incrementally, by a sequence of candidate extension steps.

\- Conceptually, the partial candidates are represented as the nodes of a tree structure, the potential search tree. 

\- Each partial candidate is the parent of the candidates that differ from it by a single extension step; the leaves of the tree are the partial candidates that cannot be extended any further.

\- The backtracking algorithm traverses this search tree recursively, from the root down, in depth-first order. 

Every wrong solution is a “world” incompatible with the constraints

#### Stochastic search

\- Stochastic search includes simulated annealing, genetic algorithm, tabu search. 

a. Randomly assign numbers to the blank cells in the grid.

b. Calculate the number of errors.

c. ”Shuffle” the inserted numbers until the number of mistakes is reduced to zero.

A cost function evaluate the quality of the solutions. 

The search may be trapped in a valley. It may be necessary to “heat” the system. 

#### Recent contraint solvers

\- Google Optimization Tools (a.k.a., OR-Tools) is an open-source, fast and portable software suite for solving combinatorial optimization problems.

\- MiniZinc, free and open-source constraint modeling language[free and open-source constraint modeling language](http://www.minizinc.org/)

\- Recent Deep learning based constraint solvers

### What are the "constraints” for History ?

#### Constraints about events

Usually Spatiotemporal constraints. Two actors must be at the same time and in the same place to interact. Two actors must exist in the same time interval to interact (see previous course)

#### Many other kinds of constraints

\- Rules of Physics

\- implicit common sense rules (The subject of Cyc modelling)

\- Specific Cultural rules (e.g. Who can marry who) … 

\- Other complex and evolving systems of rules

#### Regimes of infelicity

“it is necessary to accept that there are several regimes of truth, several types of reason, several modes of existence for which the investigator must carefully draw up the conditions of bliss and infelicity.” 

\- Bruno Latour, Enquête sur les Mode D’Existence

Science, Law, Politics, Religion, Economics have their own independent felicity regimes. 

When they intersect problem occur. 

Ex : Bertrand Cantat

## Rule systems

cf Rules of Play.

### Explicit and implicit rules

The four rules of Tic-Tac-Toe

\- Play occur in a 3 by 3 grid of 9 empty squares

\- Two player alternate marking empty squares, the first player marking Xs and the second players marking Os

\- if one player places three of the same marks in a row, that player wins, 

\- If the spaces are all filled and there is no winner, the game ends in a draw. 

Is the game well defined ?

There are also implicit rules 

\- Can I wait more than 20 seconds between turns ?

\- Can I refuse to play the next move ?

\- Can I play not using a piece of paper but on the asphalt of a super dangerous high-way. 

There are plenty of unwritten rules

### Rule systems isomorphisms

####  3-to-15 Mental Calculus Game

\- Two players alternative turns

\- On your turn pick a number from 1 to 9

\- You may not pick a number that has already been picked by either player. If you have a set of exactly 3 number that sum 15 you win

#### Guilk card game

\- A card game defined buy Evgeni Guilk

\- The following words are placed on cards : REVE, GROG, RAT, VIS, SAGE, STUC, VAN, BING, NET

\- Each player pick a card in turn. 

\- The first player to have three cards with a common letter win. 

#### Isomorphism

Tic-tac-toe, 3-to-15 and the Guilk game are formally identical. The same winning strategy works for the three. A computer may play them in the same way. 

Same formal game, same solution but different experiences …

How many other real-world games / system of rules are isomorph to this class ?

### Typologies of rules

**Operational rules** are the guidelines players require in order to play. 

**Constitutive rules** are the underlying formal structures of the rule systems. Some games are isomorphic in terms of constitutive rules

**Implicit rules** are the “unwritten rules” of a game concerning etiquette, good sportsmanship and other implied rules of proper game behaviour.  

If we adapt this to historical modelling : 

**Operational rules** -> explicit rules that entities and relation should respect. (e.g. In many culture, a father cannot marry his daughter, some actions are prohibited by give laws)

**Constitutive rules** -> underlying formal rule systems linked with morphism with operational rules 

**Implicit rules** ->  common sense functioning of the world and implicit behaviour norms.  

### Metasolvers

Depending on a set of rules, finding a possible solution / compatible world or finding all the possibles solutions / compatible worlds is potentially a hard problem. 

One domain of Symbolic Artificial Intelligence is concerned with learning how to solve problems in a general manner i.e. developing Metasolvers. The system learn to classify classes of problems and reapply the same strategies when it faces similar situations (i.e. isomorphic constitutive rules)

One of the key intuition of Jacques Pitrat (1934-2019) was that it is possible to bootstrap more and more powerful constraint solvers / theorem provers by letting the machine develop its own strategy for learning. 

## Rules complexity

### Order 0

Zeroth order logic (Propositional logic) deals with [propositions](https://en.wikipedia.org/wiki/Propositions) (which can be true or false) and relations between propositions, including the construction of arguments based on them. Propositional logic does not deal with non-logical objects, predicates about them, or quantifiers. However, all the machinery of propositional logic is included in first-order logic and higher-order logics. In this sense, propositional logic is the foundation of first-order logic and higher-order logic.

Premise 1: If it's raining then it's cloudy.

Premise 2: It's raining.

Conclusion: It's cloudy.

Both premises and the conclusion are propositions. The premises are taken for granted, and with the application of **modus ponens** (an inference rule), the conclusion follows.

Propositional logic was developed into a formal logic (Stoic logic) by Chrysippus in the 3rd century BC. 

The system was essentially reinvented by Peter Abelard in the 12th century.

In the 17th century, Gottfried Leibniz formalised it as symbolic logic

Many of the advances achieved by Leibniz were recreated by logicians like George Boole and Augustus De Morgan in the 19th century. 

### Order 1

Consider the two sentences "Socrates is a philosopher" and "Plato is a philosopher". 

In propositional logic, these sentences are viewed as being unrelated, and might be denoted, for example, by variables such as p and q. 

The predicate "is a philosopher" occurs in both sentences, which have a common structure of "a is a philosopher". 

The variable a is instantiated as "Socrates" in the first sentence, and is instantiated as "Plato" in the second sentence. While first-order logic allows for the use of predicates, such as "is a philosopher" in this example, propositional logic does not.

First-order logic allows the use of sentences that contain variables, so that rather than propositions such as 

"Socrates is a man", 

one can have expressions in the form 

"there exists x such that x is Socrates and x is a man", 

where "there exists" is a quantifier, while x is a variable

It is also possible to write rules like :

"if a is a philosopher, then a is a scholar". 

The foundations of first-order logic were developed independently by Gottlob Frege and Charles Sanders Peirce.

### Order 2

First-order logic quantifies only variables that range over individuals

Second-order logic, in addition, also quantifies over relations. 

First-order logic can quantify over individuals, but not over properties. 

We can take an atomic sentence like Cube(b) and obtain a quantified sentence by replacing the name with a variable and attaching a quantifier

∃x Cube(x)

But we cannot do the same with the predicate. That is, the following expression:

∃P P(b)

is not a sentence of first-order logic. But this is a legitimate sentence of second-order logic

As a result, second-order logic has much more “expressive power” than first order logic does. 

For example, there is no way in FOL to say that a and b have some property in common; but in second-order logic this would be expressed as

∃P (P(a) ∧ P(b)).

### Higher order

More complex logics exist. 

Among them, Lambda calculus : combination of predicate logical function with richer calculus

### Fuzzy logic

See Zadeh

## Creation of new facts and new rules 

### Creation of new hypothetical facts

What type of reasoning can one use for adding hypothetical new facts (triples) to an existing database ?

#### Forward : Deduction

Feed-forward chains of reasoning. 

If all premises are true, the terms are clear, and the rules of deductive logic are followed, then the conclusion reached is necessarily true.

All men are mortal. (First premise)

Socrates is a man. (Second premise)

Therefore, Socrates is mortal. (Conclusion)

#### Backward : Abduction

Abductive reasoning is the inference to the best explanation. 

It is like solving a crime scene. The best possible explanation is often defined in terms of simplicity and elegance.

For instance: it is a known rule that, if it rains, grass gets wet; so, to explain the fact that the grass on this lawn is wet, one abduces that it has rained.

### Creation of new hypothetical rules

#### Inductive generalisation

An inductive generalisation proceeds from a premise about a sample to a conclusion about the population.

The observation obtained from this sample is projected onto the broader population.

if all swans that we have observed so far are white, we may induce that the possibility that all swans are white is reasonable

#### Conjecture generations and selection

Inductive reasoning has been highly criticised in particular by Popper.

Instead, Rules can be created as conjectures that get refined and selected when “tested” on new datasets / observations.

This progressively leads to “Objective Knowledge” 

Rules/conjecture evolution are generated through as being shaped by variation and selection like living species. 

Rules that create more constraints and therefore limit the number of possible worlds are automatically preferred. 

The complexity of the rules can also be taken into account (e.g. Kolmogorov complexity )

## Simulation

### Procedural worlds based on rule systems

Given intermediary observations (initial and intermediation conditions) and a set of (progressively extended) rules, it is possible not only to detect incoherence and logical contraction but also to simulate possible worlds. 

Considering for instance a grid world (more simple equivalent of our 4D grid), one can study the space of possible histories. However, complexity can rapidly explode. 

### Conway's Game of Life

At each step in time, the following transitions occur:

\- Any live cell with fewer than two live neighbours dies, as if by underpopulation.

\- Any live cell with two or three live neighbours lives on to the next generation.

\- Any live cell with more than three live neighbours dies, as if by overpopulation.

\- Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.

The initial pattern constitutes the seed of the system. 

The first generation is created by applying the above rules simultaneously to every cell in the seed; births and deaths occur simultaneously, and the discrete moment at which this happens is sometimes called a tick. 

Each generation is a pure function of the preceding one. The rules continue to be applied repeatedly to create further generations.

Why does the Game of Life interest us?

\- The emergent dynamics shapes are the result of determinist history (cf. Leyton’s Shape = History)

\- Shapes are created by creation of asymmetries

\- Stability of certain forms is emergent (and not hard coded) into rules. 

### Procedural games

> Definition: A procedural representation is a process-based dynamic form of depiction. 

The Game of Life is a simple version of a procedural game.

Simple procedural rules lead to complex emerging world 

Sim City is a also a procedural game dealing with more complex urban processes, city economics, evolution of communities. 

Likewise for the Sims or Spore …

Example of games by Will Wright

### Simulations as inversed procedural models

> Definition : A simulation is a procedural model of aspects of “reality”. 

This procedural representation works at a given level of abstraction. 

The term is sometimes ambiguous denoting both the process and the results of the process. 

The goal is to design the procedural rules that will fit the observation data all level. 

It is an inverse procedural problem (like the one we saw for 3D procedural modelling)

It contains two challenges that can be addressed at different level of abstraction. 

\- Finding the right parameter for rules

\- Finding the right rules. 

Can both be induced / conjectured by Artificial Intelligence system ?

### Simulats : Simulations results as stable objects

Simulations are both process and products. The name is ambiguous. 

Large-scale simulations like the one done in biology (Human Brain Project, Simulation of the Earth) are changing the weigh between the simulation formal system and the simulation results. In traditional simulation, the results are usually only used for future validation or prediction but do not constitute stable and debated knowledge objects. 

With large-scale integrative simulation, simulation results become stable objects in themselves and not just temporal output of computation of a model. 

> Definition : A Simulat is a stable and consensual instance of a simulation. 

The best version of “reality” we have so far. 

But nevertheless, an object of study and negotiations. 

An historical simulat maybe compared with what we know about the past and the future and criticise based on knowledge and observation.

It leads to change of rules and parameters in the simulation and therefore to a new simulat. 

Two factors therefore contribute to the evolution of the Simulat: new data and new constraints that redraw the landscapes of the cost function and the search for the optimium of the function. It is indeed not easy to find the version of the past and the future that best optimises all the constraints and better accounts for the existing data.

### Heating simulats

Like for other optimisation problem, the Simulat can in part be blocked in a valley of potential. All the variations around the solution lead to a deterioration of the coherence constraints but there is nevertheless a better solution elsewhere, further in the configuration space. 

The difficulty is that its origin is based on relatively different hypotheses concerning the past and the future.

To explore these other configurations, it is necessary to "heat" the the graph, increase its temperarature and allow more distant appearances and transitions. 

Warming up the graph is obviously a culturally delicate situation because it is nothing more and nothing less than questioning the consensual versions of the past and future, the old Simulats, to look for a potentially better configuration. Some historical "facts", some solid "predictions" could be questioned in this process in this moment of cultural instability. 

During the period of reheating, a large part of our certainties are called into question, in search of a more satisfactory configuration of the world as a whole. 

## Parallel worlds and Fictional spaces

The Simulat is only one of the many possible parallel worlds, the one we collectively agree as being the most probable. A particular version of the past and the future compatible what we know and understand. 

World bifurcations like in chess.

### Thinking the plurality of worlds

Cf David Lewis, Pierre Bayard

### Uchronies

cd K.Dick

### Reality of Parallel worlds

cf David Deutsch

### Fictional spaces

Return on the notion of Fictional Spaces

Many fictional spaces exist at the same time. 

Many fictional spaces continue to exist event after some disambiguitation. 

## Summary

The core challenge for processing billions of extracted information is to develop process to induce new rules, deduce and abduce new facts and ultimately produce a continuously revised consensual version of the past and the future, the Simulat. 

The Simulat is one of the fictional spaces. 

## In the next chapter

We will introduce a hidden dimension of knowledge : sub-conceptual information. 

## Further Reading

- Latour, Enquete sur les modes d'existence
- Patricia Martin-Rodilla, Diggitng into software knowledge Generation in Cultural Heritage
- Goertzel, Geisweiller, Coelho, Janici, PEnnachin, Real-word reasoning : Toward Scalable, uncertain spatiotemporal, contextual and causla inference
- Simonis, Helmut (2005). "Sudoku as a Constraint Problem". Cork Constraint Computation Centre at University College Cork: Helmut Simonis. [CiteSeerX](https://en.wikipedia.org/wiki/CiteSeerX_(identifier)) [10.1.1.88.2964](https://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.88.2964). paper presented at the Eleventh International Conference on Principles and Practice of Constraint Programming
- Jingchao Chen, *Solving Rubik’s Cube Using SAT Solvers*, arXiv:1105.1436, 2011.
- Biere, A., Heule, M., and van Maaren, H. *Handbook of satisfiability*, volume 185. IOS press, 2009a
- Knuth, D. E., *The art of computer programming*, Volume 4, Fascicle 6: Satisfiability. Addison-Wesley Professional, 2015
- Vipin Kumar, *Algorithms for constraint-satisfaction problems: a survey*, AI Magazine Volume 13, Issue 1, 1992.
- Jacques Pitrat, Metaconnaissance
- Alfred Tarski, 1946, /Introduction to Logic and the Methodology of Deductive Sciences/, Dover Publications, Inc, New York NY, ( [ISBN](https://fr.m.wikipedia.org/wiki/International_Standard_Book_Number)   [0-486-28462-X](https://fr.m.wikipedia.org/wiki/Sp%C3%A9cial:Ouvrages_de_r%C3%A9f%C3%A9rence/0-486-28462-X) ). ( [lire en ligne](http://sistemas.fciencias.unam.mx/~lokylog/images/stories/Alexandria/Oxford%20Logic%20Guides/%5BOLG%2024%5D%20Introduction%20to%20Logic%20and%20to%20the%20Methodology%20of%20the%20Deductive%20Sciences%20-%20Alfred%20Tarski%20%5BOxford%20Logic%20Guides%5D%20%281994.4ed%29%28T%29.pdf) )
- Alfred Tarski, 1983 (1956). /Logic, Semantics, Metamathematics/, Corcoran, J., ed. Hackett. 1st edition edited and translated by J. H. Woodger, Oxford Uni. Press.
- David Deutsch, The Fabric of Reality 
- David Lewis, De la pluralité des mondes
- Aaronson, S. Quantum Computing Since Democritus 
- Pierre Bayard, il existe d'autres mondes
- Karl Popper, un univers de propensions
- Bruno Latour, irreduction

## Possible additional references

- Why Deep Learning stuggle wih the Game of Life : https://bdtechtalks.com/2020/09/16/deep-learning-game-of-life/

## Currenty Not used (maybe to move somewhere else)

Early logic : Finding the rules of reasonning

- Zeno, Plato and Aristotle
- Stoic propositional logic
- Rigveda and inductive Nyaya logic

Early moden area

- Sanctius : A new syntactic thoery based on four operators
- Port Royal grammarians. La nouvelle methode pour facilement et en peu de temps comprendre la lanauge latine (1644)
- Valla, Ramus and Port Royal : Formal vers natural logic. De falso credita (Valla)
- New artifical languages : Bacon, Dalgarno and Wilkins
- Symbolic Logic : Leibniz. De arte combinatoria (1666)
- Linguistic and logic in China

Logic in the 19th and 20th century 

- During the ninenteenth century, logic developed in a direction of a meta-mathematical diciopkine with the work of Goerge Boole (1815-1864), 
- Gottlob Frege (1848-1925) developed predicate logic and is considered the most importatn important logician since Aristote. The truth value of a complex sentence can be computed on the basis of the truh value of the elementary propositions that make that sentence. 
- This is called the princple of compositionnality (already expressed by the Indian philosopher Yaska)
- Predicate logic is the basis of more complex richer logics like modal logic and more refeindes systems of meaning referecnes (e.g. intensioanl logic)

Generative linguistics : Harris and Chomsky (maybe to move to Writing Systems Chapter)

- Chomsky's Syntactic Structure (1957) : a system of rules is needs to correctly generate all grammatical sentences rahter a structuralist system of "relation of differences". A grammar in the sense of Panini. Context-free grammar. 
- Chomsky makes a difference between performance (language use) and competence (language knowledge) . Aspect of a theory of syntax)
- This lead to the hierachy of formal languages (Three models for the description of language)
- Zellig Harris (1909-1992) had also developed a grammatical formalism known as context-free gramar. The derme contexte-free is in contract with Panini's context-sensentisive grammar (Zellig, Harris, methods in structual linguistics)
- Chomsky simplified his lniguistic theroy until he reacehd his Minimlsit Programm (1995) made of just a single combination operation, called merge. 

From Frege to Montague : Integration of linguistics and logic

- As early as Syntactic Structure (1957), Chomsky kept semantics out of the agenda. 
- The integration of linguistics and logic is one of the major achievemetn of the 20th century with effects from musicoloyg to literary studies. 
- Lambda calculus : combination of predicate logical function with richer calculus
- Montague (1930-1971) : English as a formal language (1970). The combination of three formalism : Predicate logic, Generative Grammar and Lambda Calculus leads to a new logical grammar knowm as teh Montague Grammar. However, little impact. Montague Grammar formed a school in its own right. 

Shortcomings and the rise of computational lninguistics (Rens Bod)

Categorial vers gradient aspects of language and the notion of probabilistic grammar

- There is a continuum between gramamtical and ungrammatical sentences, as well as standard and non standard language use. 
- We arrive at a theory which is statistical by nature. This lead to probabilistic grammar. 
- Also usage-based grammar and construction grammar. See Rens Bod, Beyond Grammar: An experience-based theory of language. 

Compactness versus redundancy of grammars

- Chomsky and the other generativists watnt to ahve their grammar as small as possible 
- But human language seems to be highly redundent
- In computational lingusitics most succesful applciatiosn are bbased on statistical genaratalisaiton from examples 
- Typologies of languages : free versus strict word order. Free word order language seem difficult to map with contempory grammars. 

Recent developments

- Optimalisty theory for generative grammars
- Examplar theory for statistical approaches
- Discourse representation theory for logical semantics
- A stricking lack of unity. 



