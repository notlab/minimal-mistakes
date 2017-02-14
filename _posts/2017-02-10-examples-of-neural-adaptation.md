---
title: "Examples of Neural Adaptation"
categories:
  - Computational Neuroscience
tags:
  - neural-adaptation
  - mechanoreceptors
  - pyramidal-cell
---

In this note we investigate how the [firing rate response](https://en.wikipedia.org/wiki/Neural_coding#Coding_schemes) of certain neurons
adapts to a constant input stimulus. In particular, we look at the [neural adaptivity](https://en.wikipedia.org/wiki/Neural_adaptation) of frog 
[mechanoreceptors](https://en.wikipedia.org/wiki/Mechanoreceptor) and neocortical 
[pyramidal neurons](https://en.wikipedia.org/wiki/Pyramidal_cell).

### Firing rate adaptivity in mechanorecptors

Skeletal muscles in frogs contain "muscle-spindles", which are sensory nerve fibres wrapped in modified muscle tissue. In the example spindle 
pictured below[^1] we see where the sensory nerve fibres meet with the muscle fibres. Spindles of this form allow the frog to detect 
when its muscles are stretched in the axial direction. 

![Example frog muscle spindle]({{ site.url }}/assets/images/neuro/muscle-spindle.jpeg){: .center-image }

Using a procedure designed by [Keith Lucas](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1533646/), it is easy to isolate and manipulate a frog's
sterno-cutaneous muscle. The sterno-cutaneous is a small muscle that attaches to the frog's sternum on one end and to its skin on the other. 
In most frogs this muscle contains three or four muscle-spindles. A muscle that has been isolated using Lucas' procedure is pictured below.[^2]

![Keith Lucas' experimental setup]({{ site.url }}/assets/images/neuro/keith-lucas-setup.jpeg){: .center-image }

Using this setup, [Adrian and Zotterman](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1514782) were able to record how sterno-cutaneous sensory 
neurons respond to various types of stretching. They obtained the electrograph below by hanging a 1 gram weight from the muscle and recording 
the response generated in a single afferent nerve fibre.[^3] 

![Regular spike train]({{ site.url }}/assets/images/neuro/regular-neural-series.jpeg){: .center-image }

So it would appear that hanging a fixed weight produces a regular firing response in our stretch-sensing neuron. Further experiments with 
different weights confirm this fact. It turns out that, once a certain threshold is passed, different weights trigger different firing 
frequencies. As can be seen in the electrograph below, gradually increasing the amount of weight on the muscle results in an increased firing 
frequency. This is a fairly standard example of rate coding, whereby a neuron encodes information in its firing rate. 

![Increasing frequency spike train]({{ site.url }}/assets/images/neuro/incr-neural-series.jpeg){: .center-image }

All of the experiments we have considered so far look at the response profile in the first few seconds after the weight is hung. If we leave
the weight hanging for a long time, the response we observed initially will gradually change until it seems to settle into a regular pattern.
Plotting firing frequency against time for muscles stretched by 0.5 and 3 gram weights reveals a power-law type dependency:[^4]

![Power-law neural adaptation]({{ site.url }}/assets/images/neuro/adaptation-power-law.jpeg){: .center-image }

This power-law change in firing response is our first example of neural adaptation.



[^1]: Muscle spindle image from [The Physiology of Excitable Cells](https://books.google.ca/books?id=3JgC_rE8ZVwC&lpg=PP1&dq=inauthor%3A%22David%20J.%20Aidley%22&pg=PP1#v=onepage&q&f=false) by David Aidley.

[^2]: Image from Lucas' paper [The "all or none" contraction of the amphibian skeletal muscle fibre](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1533646/).

[^3]: All electrograph images in this section are from the [Adrian and Zotterman paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1514782).

[^4]: This graph is also from [Adrian and Zotterman](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1514782). 
