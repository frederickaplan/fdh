---
title: 'Foundations in Digital Humanities 4.6'
subtitle: 'Mirror World'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Mirror World

## Concepts

### Mirror Worlds and 4D

Digital epiderm. 

The mirror-world will aim to be an up-to-date model of the world as it is, as it was and as it will be.

All objects (including representations of landscapes) of the mirror-world will be machine-readable, and, therefore, searchable, traceable and available to be part of simulations by powerful algorithms. In the mirror world, time will be a fourth dimension, as it will be very easy to go back to the past, at any location, reverting to a previous version kept in the log. One may also travel in the other direction, as future versions of a place can be artificially created based on all information available that can be used to anticipate a predictable future. Such “time-trips” will have an increased sense of reality, as they will be based on a fullscale representation of the present world.

Augmented Reality. 



## Real-time streaming

Note from Bachelor thesis : 

Web technologies have several ways to display graphical content. Such content can either be internally generated from the web browser or received from a web server ready to be displayed.

For the first option where content is graphically rendered on the client’s machine on a browser, web technologies currently offer a limited amount of graphical rendering capabilities. Apart from static image files and Scalable Vector Graphics (SVG) files, HTML5 and JavaScript offer a Canvas onwhich programs can dynamically draw either with a simplified JavaScript API (Canvas API) or with a lower level graphical API: WebGL. Because of the very basic capacities of the former, we only will discuss about WebGL as an alternative to an OpenGL application. This option allows developers to draw images of 3D scenes in real time using a set of graphical commands to communicate with the machine’s Graphics Processing Unit (GPU). This type of solution is convenient to develop, as technologies in question are high level and fast to develop. This also relieves the developer of the application of having dedicated hardware to render the display, as it is the client machine’s task. The main drawback is that, as discussed in the next chapter, there are some performance losses due to layers of abstraction.

Plus : Simpliciity but 

Minus : no multithreading  not good perfomance because of Javascript 

The second option avoids needing the client to do the graphical computing, but instead needs a dedicated machine that plays the role of a rendering server. It periodically outputs images of the rendering process which can be exported and sent through the network to the front-end application on the web. This allows the developer to have control over the rendering power, as the quality and performance are responsibilities kept to the maintainer of the application and not to the end-user.

PLus : Works with simple device. 

GPU Revolution 

To maintain a scalable service of 3D rendering over the network, the maintainer can take advantage of cloud services that offer dedicated machines with high-end GPUs and take care of the hardware maintenance in case of failure or simply upgrades to newer materials. As the rendering engine is not limited toWebGL, the rendering engine could be developed with better optimized systems. Developing the engine at a lower-level means we can avoid data abstractions and some transfer flows during the process, to achieve better performance than Web. This of course have several drawbacks, the first being the cost of the service: there is another server to maintain online and which needs processing scalability on users demand. This is also a solution that demands more work put in the development of the application, needing knowledge in three different fields: low-level graphics programming, fast networking structures and web front-end application. In the time span of this project, a prototype was achieved that can be improved and completed in all three aspects.

Big question : Two scenarios : 

- Above the Web
- Under the web

## Practice

## Question and Answers 

## Further Reading
