---
title: Introduction to waveshaping
author: Nico
date: 2020-06-30 15:45:00
categories: [Pure Data]
---

Waveshaping is a distortion technique that allows us to modulate a signal amplitude, controlling the way that the amplifier processes the waveform by using a non-linear transfer function.

An amplifier is used to increase the voltage, current, or power of a signal and amplifiers have a transfer function, which is basically a graph relating the input to the output of a signal. 

A linear transfer function is a straight line and will leave a given signal unchanged, if you for instance increase the amplitude of the input signal by 2 it will double the output signal. However, a deviation from that straight line will introduce distortion. Having control over that amount is musically interesting since waveshaping is an efficient way to create complex timbres. With a non-linear transfer function we can create different waveform shapes by altering the transfer function shape. This will allow you to play around with the spectrum and harmonic content of the waveform.

In pure data, there is an object called [clip~] and what clip does is to pass a signal input to the output, clipping it to lie between two limits (you can check this with details in the help patch), which you will specify by giving it two arguments. [clip~] will pass the input to the output unchanged as long as it stays between the limits we established.

![clip-object](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/IntroWaveshaping/Fig1_Clip-object.png){: width="170" height="150" }
_Fig.1 Giving arguments to [clip~]_

![waveshaping-vs-linear](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/IntroWaveshaping/Fig2_waveshaping-vs-linear.JPG){: width="510" height="518" }
_Fig.2 Difference between an unchanged signal and a clipped signal_

The new shape you will create on your output depends on different things:
 - transfer function
 - shape of the incoming wave
 - amplitude of the incoming signal 

The amplitude of the incoming waveform is called the waveshaping index. The index provides continuous control of the spectrum making possible dynamic spectra through time variation. A small index will generally introduce little distortion, as the index is increased the spectrum becomes richer, see Puckette, 2007.

I'll show you how you can observe this with pd:

![ws-linear](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/IntroWaveshaping/Fig3_waveshaping-vs-linear-2.JPG){: width="710" height="454" }
_Fig.3 Waveshaping vs linear_

### Video demonstration

<div style="text-align: center;"><iframe width="560" height="315" src="https://www.youtube.com/embed/q3vaxSWWWg8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>


### References

Dodge, Charles, and Thomas A. Jerse. Computer music: synthesis, composition and performance. Macmillan Library Reference, 1997.\
Puckette, Miller. The theory and technique of electronic music. World Scientific Publishing Company, 2007.\
Russ, Martin. Sound synthesis and sampling. Taylor & Francis, 2004.



