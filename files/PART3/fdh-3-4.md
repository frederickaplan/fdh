---
title: 'Foundations in Digital Humanities 3.4'
subtitle: 'Non conceptual knowledge systems'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Non conceptual knowledge systems

## Theses

The recent successes of Deep learning changed the rules of the AI game. For Digital Humanities, it opens an avenue a new possibilities. Deep learning offers new ways for detecting patterns, i.e. for compressing information, i.e. for understanding, i.e for generating new representations following the same patterns. It can also be used to take decisions optimising some well defined cost function.

Will the Most advanced deep learning, combined with Big Data of the past lead to the Most advanced AI even made ?

The theses explored in this chapter are the following :

1) Deep learning offers new ways for encoding / decoding writing systems and images

2) This can be used to enrich and bootstrap extacted datasets

3) This produce a new family on non conceptual knowledge

## Articulated reasoning and Non conceptual knowledge

We can define non conceptual knowledge in a negative manner.

> Definition : Non conceptual knowledge is knowledge that is ***not\*** framed in terms of discrete set of articulable concepts.

Articulated reasoning is based on some specific characteristics :

- **Identity / non identity** : “The killer is not my brother Jim”
- **Quantification**: "Every French person eats fresh bread"
- **Variables** : "Marriages in which one person is much older than the other"
- **Logical operators** : And, not/negation, implies “No classical violinists like football”
- **Sets** :The president, the vice-president and the White House staff”, “All living animals”
- **Intensional contexts** : "She said the Switzerland has a king"
- **Categories and subcategories** : "Among those who were invited”
- **Possibility and Necessity** : “She might have gone to the United States”
- **Default reasoning**: “Unless otherwise noted, the number of students must be considered in the design of the classroom”

Articulated reasoning can be modelled with logical formalism like we viewed in previous courses.

The main issue is the “grounding” of real world data into logical symbols.

Disambiguating entities is hard.

Inducing rules directly from the data is even harder.

Architecture not based on conceptual articulation have managed in practice to perform very complex task, some of which ressemble articulate reasoning.

How is this possible ? How is there non conceptual knowledge stored ? Can we use it in additional to articulate reasoning ?

Non conceputal knowledge

- is not chopped up into neat, ontological objects
-  derives more from large continuous dynamic process rather that a small number of logical steps
- is progressively constructed in a bottom up manner out of the data and not vice-versa.
- Capture understanding that humans may not have understood yet.

## Recent success of non conceptual knowledge systems (2012-2020)

### Object visual recognition

ImageNet challenge : An image system of 1.3 Million images (annotated by hand)

AlexNet (2012) : 60 M parameter neural network which go way better than any other approach.

Critics : Deep learning is just about perception …

### Machine translation

2015 : A 380 M parameter neural network mapping input sentence in one language to output sentence in another.

Now powers all modern translation engines

Critics : Deep learning progress is driven / limited by labelled datasets.

2018: \- A 117 M parameter “transformer” trained by reading 7000 self-published books beating with very limited supervised fine training most state-of-the-art approach..

Unlabelled datasets may be more important than labelled

Critics : Deep learning is about static datasets.

### Games

2013 : A 150 000 parameters feed forward network trained to play an number of Atari games purely from pixels and scores. (https://www.youtube.com/watch?v=V1eYniJ0Rnk)

Discovery of optimal solution for playing games

Critics : These are simple games. Reinforcement Learning can’t solve hard tasks

2016 : A 72 M parameter feed forward network to defeat humans at Go

Critics : It’s just imitation of human expertise and brute force.

2017 : AlphaGo Zero plays again itself and invents non human moves. The way human play the game of Go is suboptimal for centuries.

Freed from tradition and imitation, AlfaGo Zero discovered new possible “cultural spaces”.

This remind of the notion of **“Intinite fun space”**

Iain M. Banks’s Culture series "The mental capabilities of Minds are described in Excession to be vast enough to run entire universe-simulations inside their own imaginations, exploring metamathical (a fictional branch of metamathematics) scenarios, an activity addictive enough to cause some Minds to totally withdraw from caring about our own physical reality into "Infinite Fun Space", their own, ironic and understated term for this sort of activity. (wikipedia)"

The Infinite fun space is huge. Humans have only explored a little of it.

Centaurs : Human and nonhuman moves

\- Kasparov and the Centaurs.

\- Will there be centaurs for Go ?

\- Will there be centaurs for the humanities ?


Side note on chess: AlphaZero, which is now unquestionably superior to previous game engines, has (independently) rediscovered a very elegant, dynamic, and human-like play style; while previous engines had a cold, machine-like style. To be mentioned in the "cultural space" paragraph?

## Fundamental principles and their progressive implementation

### Simple neuron and perceptron

McCulloch, W. S. and Pitts, W. 1943. A logical calculus of the ideas immanent in nervous activity. Bulletin of Mathematical Biophysics 5:115–133.

Rosenblatt, F. 1957. The Perceptron — a perceiving and recognizing automaton. Report 85–460–1, Cornell Aeronautical Laboratory.

### The perceptron controversy

cf. Olazaran, A Sociological Study of the Official History of the Perceptrons Controversy.

- 1959 : New York Times : “The Navy revealed the embryo of an electronic computer today that it expects to be able to walk, talk, see, write, reproduce itself and be conscious of its existence. Later perceptrons will be able to recognise people and call out their names and instantly translate speech in one language to speech and writing in another language, it was predicted”

- 1969 : Publication of Perceptrons by Minsky and Papert.
- Papert in 1988 : “There was some hostility in the energy behind the research report in Perceptrons, Part of our drive came, as we quite plainly acknowledged in our book, from the fact that funding and research energy were being dissipated on … misleading attempt to use connectionist methods in practical applications”
- Minksy in 1989 : “In the last 1950s and early 1960s, after Rosenblatt’s work, there was a great wave of neural network research activity. There were maybe thousands of projects. … They were trying to get money to build bigger machines, but they didn’t seem to be going anywhere”

### Neural networks revival

In the early 1980s, dramatic decreases in computing costs lead to a democratisation of computing resources.

Rummelhart, Hinton, McClelland …

Conceptualisaiton of the notion of receptive field

Hierachical representation / textures

Pyramid of neural abstraction : from perception to emergent concepts.

For shaping networks.

- Credit assignment paths
- Gradient descent algorithm.

## Convolutional neural networks

\- Some of the receptive fields of the network are convolutional units/filters.

\- The image become a stack of filtered images

\- Pooling : Shrinking the image stacks

\- Rectified Linear Units (ReLUs)

\- Control through Hyperparameters (knobs) : Convolution (Number of features, size of features), Pooling (Window size, Window stride), …

Convolutional neural networks do not work only on images.

\- Work on any 2D or 3D Data

> Locality Principle : Things close together need to be more closely related than things far away.

## Encoding / decoding writing systems

\- Encoding a sequence in another sequence

French -> English

Question -> Answer

First words -> Full paragraph

Natural Language description -> Programming code

One Writing System -> Writing System

Natural Language description -> First order logic predicate ?

Natural Language description -> RDF ?

### Recurrent neural networks

\- Recurrent neural networks are used to process sequences (text, audio)

\- Inputs are processed one at a time, updating an internal state.

\- Allows single_state->sequence, sequence->single_state, sequence->sequence

\- Example of recurrent cells : LSTM, GRU, bidirectional RNN

\- RNN can represent most of grammars for any information embedded in time.

\- In principle RNN are the deepest of all the networks.

\- RNN can be considered general computers that can process memories of any sequences of patterns.

Limitation of RNN : RNN do not scale well for long sentences (they forget the beginning of the sentence when they arrive to the end …)

The way a RNN works can be understood by taking the analagoy of a buck of water (cf Liquid State Machine). Data is dropping in the water but the memory of the water waves only last for a limited moment. For a short time, the water is capturing a complex context (complex sitautions of waves), but it does not adapt this understanding to the situation. 

### Transformers

\- To avoir the RNN memory deficit, Transformers introduced an Attention mechanism.

\- The attention-mechanism looks at an input sequence and decides at each step which other parts of the sequence are important.

\- An architecture with only attention-mechanisms and without any RNN (Recurrent Neural Networks) can improve on the results in translation tasks

\- Transformer model facilitates more parallelization during training. They enabled training on larger dataset.

First article introducing the Attention mechanism : Neural Machine Translaiton by joinly learning to align and translate

Standford group reuses the ideas from Montreal : Effective appraoches to attention-based neural machine translation

Google team uses attention at a large scale  : Attention is all you need

Google again develop BERT model, Introduce Self-supervises learning (hide 10-20% of words and learn to predict the missing words) Published on arXiv on Oct 2018. 600 citations before publication at ICLR in may 2019. : BERT : Pre-training of Deep Bidirectional Transfomers for Language Understanding

GLUE and SUPERGLUE competition. These competition use in particular Winograd schemata including sentences with ambiguity :

- “The statue cannot enter in the box because it is too big”
- “The statue cannot enter in the box because it is too small”

GPT-3

- Developed by OpenAI
- 175 billion machine learning parameters.
- Need 175 Gigaoctets of RAM (impossible to run on a desktop computer)
- Trained on CommonCrawl, Wikipedia and other
- Only for English (contrary to BERT)

GPT-3 Captures the Textures of texts . Where does textures stop, where does content start.

Case studies

- Text generation with "A peek inside the attention economy"
- Layout to Code transformation

GPT-3 Turing Test

Q: What is human life expectancy in the United States?
A: Human life expectancy in the United States is 78 years.

Q: Who was president of the United States in 1955?
A: Dwight D. Eisenhower was president of the United States in 1955.

Q: What party did he belong to?
A: He belonged to the Republican Party.

Q: Who was president of the United States before George W. Bush?
A: Bill Clinton was president of the United States before George W. Bush.

Q: Who won the World Series in 1995?
A: The Atlanta Braves won the World Series in 1995.

Q: What is your favorite animal?
A: My favorite animal is a dog.

Q: Why?
A: Because dogs are loyal and friendly.

Q: What are two reasons that a dog might be in a bad mood?
A: Two reasons that a dog might be in a bad mood are if it is hungry or if it is hot.

Q: How many eyes does a giraffe have?
A: A giraffe has two eyes.

Q: How many legs does a frog have?
A: A frog has four legs.

Q: Are there any animals with three legs?
A: No, there are no animals with three legs.

Q: Why don't animals have three legs?
A: Animals don't have three legs because they would fall over

less good :

Q: How many eyes does a giraffe have?
A: A giraffe has two eyes.

Q: How many eyes does my foot have?
A: Your foot has two eyes.

Q: How many eyes does a spider have?
A: A spider has eight eyes.

Q: How many eyes does the sun have?
A: The sun has one eye.

Q: How many eyes does a blade of grass have?
A: A blade of grass has one eye.

Q: How do you sporgle a morgle?
A: You sporgle a morgle by using a sporgle.

Q: How many bonks are in a quoit?
A: There are three bonks in a quoit.

Q: How many rainbows does it take to jump from Hawaii to seventeen?
A: It takes two rainbows to jump from Hawaii to seventeen.

Q: Which colorless green ideas sleep furiously?
A: Ideas that are colorless, green, and sleep furiously are the ideas of a sleep furiously.

Q: Do you understand these questions?
A: I understand these questions.

Now on historical facts

Q: Who was president of the United States in 1801?
A: Thomas Jefferson was president of the United States in 1801.

Q: What city is in the northwest corner of Ohio?
A: Toledo is in the northwest corner of Ohio.

Q: What highway do you take to get to North Lake Tahoe from Oakland?
A: Highway 80 is the highway you take to get to North Lake Tahoe from Oakland.

Q: What are Darius's abilities in League of Legends?
A: Darius's abilities in League of Legends are: Apprehend, Decimate, Noxian Guillotine, Crippling Strike, Apprehend, and Hemorrhage.

--

Q: Who did Capablanca defeat to become world chess champion?
A: Capablanca defeated Lasker to become world chess champion.

Q: Who was president of the United States in 1700?
A: William Penn was president of the United States in 1700.

Q: Who was president of the United States in 1650?
A: Richard Bennett was president of the United States in 1650.

Q: Who was president of the United States in 1620?
A: James I was president of the United States in 1620.

Q: Who was president of the United States in 1600?
A: Queen Elizabeth I was president of the United States in 1600.

---

Q: Who won the World Series in 2021?
A: The New York Yankees won the World Series in 2021.

Q: Who won the World Series in 2022?
A: The New York Yankees won the World Series in 2022.

Q: Who won the World Series in 2023?
A: The New York Yankees won the World Series in 2023.

--

Transformers can transfrom French to English, Questions to Answers, Descrption to Code. How is this non conceptual knowledge coded

## Structures of non conceptual spaces

### Embeddings

*Tomas Mikolov Kai Chen Gregory S Corrado and Jeffrey Dean. Distributed representations of words and phrases and their compositionality. Advances in Neural Information Processing Systems, pages 3111–3119, 2013.*

The Word2Vec model, a very simple model, automatically organize concepts and learn implicitly the relationships between them

Mikolov joined Facebook and worked with others researcher on the FastText project that increase significantly the performance of Word2Vec.

Works with 150+ natural languages.

### Latent spaces

Generative Adversarial Network introduced in

*Ian J. Goodfellow, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozair, Aaron Courville et Yoshua Bengio, « Generative Adversarial Networks », dans Advances in Neural Information Processing Systems 27, 2014*

Work of the nvidia group (StyleGAN)

- A style based generator architecture for Geneartive Adversarial Networks
- Analyzing and improving the Image quality of StyleGAN : Possibility of using a target image and retrive the projected latent

Some GAN issues :

Vanishing Gradients : "if your discriminator is too good, then generator training can fail due to vanishing gradients. In effect, an optimal discriminator doesn't provide enough information for the generator to make progress."

Mode Collapse : "Usually you want your GAN to produce a wide variety of outputs. You want, for example, a different face for every random input to your face generator. However, if a generator produces an especially plausible output, the generator may learn to produce only that output. In fact, the generator is always trying to find the one output that seems most plausible to the discriminator. If the generator starts producing the same output (or a small set of outputs) over and over again, the discriminator's best strategy is to learn to always reject that output. But if the next generation of discriminator gets stuck in a local minimum and doesn't find the best strategy, then it's too easy for the next generator iteration to find the most plausible output for the current discriminator. Each iteration of generator over-optimizes for a particular discriminator, and the discriminator never manages to learn its way out of the trap. As a result the generators rotate through a small set of output types. This form of GAN failure is called mode collapse."

## Encoding / Decoding Images

### Style transfer

cf Image Style Transfer Using Convoltuional Neural Networks

\- Style vs Content representation. The key finding is that the representations of content and style in the Convolutional Neural Network are well separable.

\- Generally each layer in the network defines a non-linear filter bank whose complexity increases with the position of the layer in the network.

\- To obtain a representation of the style of an input image, it is possible use a feature space designed to capture texture information. This feature space can be built on top of the filter responses in any layer of the network. It consists of the correlations between the different filter responses, where the expectation is taken over the spatial extent of the feature maps.

### Image to Image Translation

cf Image to image translation with conditioanl adversarial networks

### Unpaired Image-to-Image Translation

CycleGAN: Unpaired Image-to-image translation using Cycle-Consistent Adversarial Networks

Constrastive Learning for unpaired image-to-iamge translation

## Self-supervised predictive learning

Predict the past based on the present
Predict the bottom of the image based on the top
Predict the end of sentence based on the beginning.

Difficulties :

Modelling all the possible ending of a sentence is easy when one has access to a large number of text
Modelling the next frame of a video (a high dimension representation) is much more complex because we only have access to single example.

## Universal non conceptual representations

\- Interlinguistic space (between language)

\- Intermodal space (between text and image)

\- Image and text latent spaces

Loops :

Generating new input for bootstrapping learning

Very large extension of the “Infinite Fun Space”

cf. “I am a Strange Loop” / Douglas Hoftsatder

## Summary

1) The existence of non conceptual knowledge is demonstrated by the excellent performances of a variety of encoders / decoders

2) These systems tend to converge in universal intermodal representation spaces.

## In the next chapter

We can decide to useduniversal encoders-decoders to massively enrich data.

But we can also try to understand the underlying structure of the data coded in the universal representation engine. This is the subject of next course

## Further Reading

- Science-Fiction : Infinite Fun Space

- Deep Learning (Goodfelow et al)

- The Promise of Artificial Intelligence (Brian Cantwell Smith)

- Mikel Olazaran, A Sociological Study of the Official History of the Perceptrons Controversy
