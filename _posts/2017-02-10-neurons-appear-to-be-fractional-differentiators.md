---
title: "Neurons Appear to be Fractional Differentiators"
categories:
  - Computational Neuroscience
tags:
  - fractional-differentiation
  - neuroscience
---

In this note we investigate how the [firing rate response](https://en.wikipedia.org/wiki/Neural_coding#Coding_schemes) of a neuron 
adapts to an input stimulus. In particular, we review evidence that certain types of neuron function by computing a fractional 
derivative of their input. Examples of such neurons include various types of 
[mechanoreceptors](https://en.wikipedia.org/wiki/Mechanoreceptor), and neocortical
[pyramidal neurons](https://en.wikipedia.org/wiki/Pyramidal_cell).

As a first example of the fractional-differentiator principle we follow 
[Adrian and Zotterman](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1514782/) (A&Z) and investigate sensory neurons in frogs.

### Firing rate adaptivity in mechanorecptors

Skeletal muscles in frogs contain "muscle-spindles", which are sensory nerve fibres wrapped in modified muscle tissue. In the example spindle 
pictured below[^1], we see that the sensory nerve fibres are woven directly into the muscle fibres. Spindles of this form allow the frog to detect 
when its muscles are stretched in the axial direction. 

![Example frog muscle spindle]({{ site.url }}/assets/images/neuro/muscle-spindle.jpeg){: .center-image }

Using a procedure of [Keith Lucas](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1533646/), it is easy to isolate and manipulate a frog's the 
sterno-cutaneous muscle. The sterno-cutaneous is a small muscle that attaches to the frog's sternum on one end and to its skin on the other. 
In most frogs this muscle contains three or four muscle-spindles. A muscle that has been isolated using Lucas' procedure is pictured below.

![Keith Lucas' experimental setup]({{ site.url }}/assets/images/neuro/keith-lucas-setup.jpeg){: .center-image }

Using this setup, A&Z were able to record how sensory neurons connected to sterno-cutaneous muscle-spindles respond to various
types of stretching. Let us first investigate what happened when the muscle was stretched by hanging a 1 gram weight. Below is an
electrograph depicting the typical response to such an experiment in a single afferent nerve fibre.[^2]

![Regular spike train]({{ site.url }}/assets/images/neuro/regular-neural-series.jpeg){: .center-image }

Clearly hanging a fixed weight produces a regular firing response in the sensory neurons associated to the stretched muscle. It turns out
that different weights trigger different firing frequencies. As can be seen in the electrograph below, gradually increasing the amount of 
weight on the muscle results in an increased firing frequency. This is a fairly standard example of rate coding, whereby a neuron encodes 
information in its firing rate. 

![Increasing frequency spike train]({{ site.url }}/assets/images/neuro/incr-neural-series.jpeg){: .center-image }

So far we have been investigating how a neuron responds immediately after the application of a stimulus. However neurons show interesting
long-term behaviour as well. For instance, if a constant stimulus is applied for a long time, the firing rate will eventually decrease and
"adapt" to the new status quo.

[^1]: Muscle spindle image from [The Physiology of Excitable Cells](https://books.google.ca/books?id=3JgC_rE8ZVwC&lpg=PP1&dq=inauthor%3A%22David%20J.%20Aidley%22&pg=PP1#v=onepage&q&f=false) by David Aidley.

[^2]: All electrograph images in this section are from the Adrian and Zotterman paper.
