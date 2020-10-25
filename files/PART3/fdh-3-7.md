---
title: 'Foundations in Digital Humanities 3.7'
subtitle: 'Generative Methods'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Generative Methods

(Simulation / Wouldbe world)

## Concepts



### Image generation

Deep fake

and deep fake detection

GPT-2 for images 

Meme creation by machines 

## Produral

Houdini



## Creative AI

Creation of music, paintings, etc. 

## Fake media

Fake media is the result of an image/video modification that changes content and metadata regardless good or bad intentions. 

Deepfakes, Audiofakes, Textfakes

### Problems

- Vanishing Gradients : "if your discriminator is too good, then generator training can fail due to [vanishing gradients](https://wikipedia.org/wiki/Vanishing_gradient_problem). In effect, an optimal discriminator doesn't provide enough information for the generator to make progress."
- Mode Collapse : "Usually you want your GAN to produce a wide variety of outputs. You want, for example, a different face for every random input to your face generator. However, if a generator produces an especially plausible output, the generator may learn to produce *only* that output. In fact, the generator is always trying to find the one output that seems most plausible to the discriminator. If the generator starts producing the same output (or a small set of outputs) over and over again, the discriminator's best strategy is to learn to always reject that output. But if the next generation of discriminator gets stuck in a local minimum and doesn't find the best strategy, then it's too easy for the next generator iteration to find the most plausible output for the current discriminator. Each iteration of generator over-optimizes for a particular discriminator, and the discriminator never manages to learn its way out of the trap. As a result the generators rotate through a small set of output types. This form of GAN failure is called **mode collapse**."
- Failure to Converge: GANs frequently fail to converge

## Question and Answers 



## Further Reading

