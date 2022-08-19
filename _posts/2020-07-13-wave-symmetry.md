---
title: Waveform symmetry and timbre
author: Nico
date: 2020-07-13 10:50:00
categories: [Pure Data]
---

### Introduction

In my introductory tutorial on [waveshaping](https://nico-audio.github.io/posts/waveshaping) I told you about the possibility of building different waveforms and how that might be musically interesting. For that first tutorial, I used [clip~] to exemplify how waveshaping works, however, there are other ways to produce different transfer functions that you can use for multiple purposes.

In this tutorial I'm going to use [cos~] as a transfer function to demonstrate the relationship between waveform symmetry and tone quality or timbre. What [cos~] does is multiplying its input by 2pi and giving the cosine of the result. An important thing to remember about [cos~] is that it takes its input in cycles, so your input should range from 0 to 1. My patch is based on professor Puckette's UCSD course, so if you're interested, I highly recommend you check that out - I'll leave the link on the references section.

First, I’m going to show you visually the difference between a sine and a cosine function.

![sine-fun](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/WfSymmetry/Fig1_Sine-function-sym.png){: width="314" height="235" }
_Fig.1 Sine function symmetry_

![cosine-fun](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/WfSymmetry/Fig2_Cosine-function-sym.png){: width="297" height="211" }
_Fig.2 Cosine function symmetry_

As you can see, the "sin" function graph, is symmetric with respect to the origin - if you flip the x to negative x you still have the same y value and the “cosine” graph is symmetric to the y-axis.

### Transfer functions and harmonic content

A sine function will produce only odd harmonics whereas a cosine function will produce even harmonics. In other words, a sine function will repeat the exact same thing for its subsequent cycles and a cosine function will do one thing for half the cycle and then do the same thing backwards for the other half, like a mirror image. This symmetric relationship is important when it comes to musical intention, since sonically this will produce different results as odd and even harmonics have different tone qualities.

![sine-spect](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/WfSymmetry/Fig3_sine-function-spec-100.JPG){: width="1149" height="432" }
_Fig.3 Sine transfer function spectrum analysis_

![cosine-spect](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/WfSymmetry/Fig4_cosine-test.JPG){: width="1149" height="449" }
_Fig.4 Cosine transfer function spectrum analysis_

Note that because of its symmetry, the cosine fuction will double the frequency that we hear. What I did here was using an [osc~] to read from these two different tables and observe the results. I created an Index control and made the signal range from 1 to 100 by multiplying by 50 and then adding 51 and used [tabread4~] to read the table. How I'm drawing these functions to the table here is not relevant to the point I'm making at the moment since we're going to use [cos~] later.

![sine-function-wf](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/WfSymmetry/Fig5_sine-function-2.JPG){: width="662" height="396" }
_Fig.5 Sine function waveform_

![cosine-function-wf](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/WfSymmetry/Fig6_cosine-function-1.JPG){: width="662" height="304" }
_Fig.6 Cosine function waveform_

As you can see, the transfer function determines your control over the shape and harmonic content of the waveform. Remember that the harmonics are what makes us differentiate between two different instruments playing the same pitch.


<div style="text-align: center;"><iframe width="560" height="315" src="https://www.youtube.com/embed/K55meFGz0Yo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

### Transforming the symmetry

Now I will show you how to add some extra control to your patch, because you can transform the symmetry of the function. There is a help patch that uses the same technique in a different way, E07.evenodd.pd. And this time we won't need to read from a table, we're just using the [cos~] object instead.

![offset](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/WfSymmetry/Fig7_offset-control-patch.JPG){: width="901" height="484" }
_Fig.7 Offset control_

We're using a non-linear transfer funcion - [cos~] - and adding an offset control, so you will basically have an even/odd control and transform the symmetry of the waveform, because you are changing the point from where you start reading.

Let's take a look at the amount of control you can have over timbre with this technique.

<div style="text-align: center;"><iframe width="560" height="315" src="https://www.youtube.com/embed/K4JNFZS_74E" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

You definitely don't have to know this to make electronic music, however, this kind of knowledge can save you a lot of time in expressing your ideas because it becomes easier to understand how to reach that sound you have in your head.

### References

Russ, Martin. Sound synthesis and sampling. Taylor & Francis, 2004.\
Dodge, Charles, and Thomas A. Jerse. Computer music: synthesis, composition and performance. Macmillan Library Reference, 1997.

Links to UCSD course:\
<https://podcast.ucsd.edu/watch/wi16/mus171wi16/2/screen>\
<http://msp.ucsd.edu/syllabi/171.16w/index.htm>
