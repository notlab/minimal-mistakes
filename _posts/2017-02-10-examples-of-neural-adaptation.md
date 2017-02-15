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
[pyramidal neurons](https://en.wikipedia.org/wiki/Pyramidal_cell) in rats.

### Exmaple 1: Frog Mechanorecptors

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

### Example 2: Rat Neocortical Pyramidal Neurons

Next we look at experiments carried out by [Lundstrom, Higgs, Spain & Fairhall](http://www.nature.com/neuro/journal/v11/n11/abs/nn.2212.html)
on adaptivity in rat neocortical [pyramidal neurons](https://en.wikipedia.org/wiki/Pyramidal_cell). These are some of the largest neurons
in a rat's brain and are mainly implicated in cognition. Below is a sketch of a human pyramidal neuron[^5], which looks similar to the rat's. 

![Pyramidal neuron]({{ site.url }}/assets/images/neuro/pyramidal-neuron.png){: .center-image }

The neocortex is a thin layer of the brain. Horizontally its neurons are arranged into six layers, usually labed I through VI. As we see in the 
following diagram[^6], pyramidal neurons are found in the middle layers of the neocortex. 

![Neocortex organization]({{ site.url }}/assets/images/neuro/neocortex-organisation.png){: .center-image }

Pyramidal cells in layers II and II project their axons further into the neocortex, while those in deeper layers often have axons that project 
out of the cortex to areas like the brainstem and spinal cord. Neurons in layer IV receive most of the external connections and project locally to 
other layers of the neocortex. Vertically the neocortex is arranged into so-called 
[cortical columns](https://en.wikipedia.org/wiki/Cortical_column). These columns are sometimes thought of as the generic building blocks of 
the neocortex. 

By preparing very thin slices of a rat's brain (see below[^7]), it is possible to isolate neurons in specific layers of the neocortex. 

![Rat brain getting sliced]({{ site.url }}/assets/images/neuro/rat-brain-slice.jpeg){: .center-image }

In their experiments, Lundstrom et al used a mixture of [whole-cell patch](https://en.wikipedia.org/wiki/Patch_clamp#Whole-cell_recording_or_whole-cell_patch)
(n = 6) and [sharp](https://en.wikipedia.org/wiki/Electrophysiology#Sharp_electrode_technique) electrodes (n = 49). These electrodes can be 
used both to inject a current into a neuron, and to record the resulting electrical response. Examples of both electrode types:[^8]

![Example electrode setup]({{ site.url }}/assets/images/neuro/sharp-and-patch-electrodes.jpeg){: .center-image }

Using this setup, two types of stimulus were used to drive layer II and III pyramidal neurons in the rat neocortex. The first was a simple
square wave current (see a. below[^9]), and the second was a Gaussian noise current whose standard deviation alternated periodically between two 
values (see b. below).

![Square-wave and square-wave noise driving currents]({{ site.url }}/assets/images/neuro/lhsf-driving.jpeg){: .center-image }

Both stimuli are periodic, say of period \\(T\\). We are studying responses to constant stimuli, so each period naturally breaks
down into two intervals of interest. The first is between time \\(0\\) and time \\(T/2\\) when the neuron receives the constant low-current 
stimulus; the second is from time \\(T/2\\) to \\(T\\) when it receives high-current stimulus. 

Lundstrom et al experimented with values of \\(T\\) ranging from \\(T = 1 ~\mathrm{sec}\\) all the way to \\(T = 32 ~\mathrm{sec}\\). The
averaged firing response rates from these experiments are summarized below. Graphs **a** and **b** cover times \\([0, T/2]\\), while
**c** and **d** cover \\([T/2, T]\\). Subject to a bit of normalization, the response profiles are essentially the same for all period lengths
\\(T\\).

![Responses recording in pyramidal neurons to square-wave type stimulation]({{ site.url }}/assets/images/neuro/pyramidal-response.jpeg){: .center-image }

Notice the power-law relationship, just as in the case of the frog mechanorecptor. Note also that:

- Firing frequency trended upwards when given a constant stimulus regime occuring after a high-to-low transition.
- Firing frequency trended downwards when given a constant stimulus regime occuring after a low-to-high transition.

[^1]: Muscle spindle image from [The Physiology of Excitable Cells](https://books.google.ca/books?id=3JgC_rE8ZVwC&lpg=PP1&dq=inauthor%3A%22David%20J.%20Aidley%22&pg=PP1#v=onepage&q&f=false) by David Aidley.

[^2]: Image from Lucas' paper [The "all or none" contraction of the amphibian skeletal muscle fibre](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1533646/).

[^3]: All electrograph images in this section are from the [Adrian and Zotterman paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1514782).

[^4]: This graph is also from [Adrian and Zotterman](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1514782). 

[^5]: From the 1903 edition of [Sobotta's histology](https://babel.hathitrust.org/cgi/pt?id=mdp.39015071685536;view=2up;seq=6).

[^6]: Neocortex sketch can be found in [Gray's anatomy](http://www.bartleby.com/107/illus754.html).

[^7]: Learn to make your very own brain slices at [www.abcam.com](http://www.abcam.com/protocols/brain-slice-electrophysiology-video-protocol).

[^8]: Image from [this paper](http://jn.physiology.org/content/92/1/380) by Li, Soffe and Roberts. 

[^9]: Neuron input and output graphs in this section come from the [Lundstrom, Higgs, Spain & Fairhall](http://www.nature.com/neuro/journal/v11/n11/abs/nn.2212.html) paper.
