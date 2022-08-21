---
title: Ring modulation - exterminate, exterminate!
author: nico
date: 2020-07-20 16:30:00
categories: [Pure Data]
---

### What is it and how it works

EXTERMINATE! If you like Doctor Who, you've heard this before. I'm going to talk about the effect behind a Dalek's voice: ring modulation, also known as balanced modulation. Ring modulation is a signal processing function, a type of amplitude modulation (AM) that takes its name from the shape formed by the diodes on its analog circuit implementation. It was originally used for analog telephony.

![ring-modulator](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/RingModulation/Fig1_Ring_Modulator.png){: width="567" height="322" }
_Fig.1 Ring modulator schematic (CC BY-SA 3.0 via Wikimedia Commons)_

![daleks](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/RingModulation/Daleks_tumblr_mcyszapmEg1rucjjm.gif){: width="500" height="288" }

In ring modulation, the carrier signal is multiplied by the modulating signal. If the modulator is under the audible range, you will perceive it as a tremolo, however if the modulating frequency is within the audible range, it will produce sidebands that correspond to the sum and difference between the frequencies of each oscillator at the output. This effect can be used to modify sounds and produce robotic voices - like Daleks - and metalic, inharmonic chaotic tones, as I will demonstrate.

Let me show you what I mean by that: we're going to multiply two [osc~] objects and take a look at the spectrum produced as a result.

![sidebands-out](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/RingModulation/Fig2_output-ring-2.jpg){: width="600" height="488" }
_Fig.2 - Sidebands produced by ring modulation_

Since we're using 2 sine wave oscillators, the spectrum produced has 2 sideband frequencies. And as you can see neither of the original frequencies are present in the output spectrum.

You can use a microphone input to get that robot voice I initially told you about - your voice will be the carrier in this case. Let's add an [adc~] and amplify the signal [\*~ 10] and then multiply it by our modulator.

![ring-mic](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/RingModulation/Fig3_micinput.png){: width="508" height="456" }
_Fig.3 - Using a microphone as input_


<div style="text-align: center;"><iframe width="560" height="315" src="https://www.youtube.com/embed/QRWfme9x4-Y" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

If the oscillators frequencies are harmonically related, ring modulation will produce harmonic partials. Let's change our patch a little bit by adding another [osc~] and creating that relation to see what happens.

![harmonics-ring](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/RingModulation/Fig4_harmonics-ring-3.JPG){: width="449" height="446" }
_Fig.4 - Adding harmonic partials_

I set Carrier A to MIDI note 30, which is equivalent to 46,25Hz (F#0) and Carrier B is twice the frequency, hence 1 octave up, 92,5 Hz (F#1). The modulator (M) is set to 4x 46,25Hz or 185Hz.

Now, I'll take a break to explain something important if you're not that familiar with Pd yet: in Pd, the cold inlet (the second one) doesn't take effect until you change the value in the first inlet, so if I change the modulator frequency it won't take effect until I change the carrier frequency. The way you fix that is by using [t b f] so that any time you change the modifier it will also send a bang to the first inlet, forcing the multiplication to happen.

That being said, let's take a look at the spectrum:

![spectrum-ring](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/RingModulation/Fig5_harmonic-f-spectrum.JPG){: width="784" height="234" }
_Fig.5 - Spectrum analysis of the product_

What we have here are 4 partials:
1st: B-M = 92,5Hz (F#1)
2nd: A-M = 138,75Hz (C#2)
3rd: A+M = 231,25Hz (A#2)
4th: B+M = 277,5Hz (C#3)

### Video demonstration

<div style="text-align: center;"><iframe width="560" height="315" src="https://www.youtube.com/embed/iMHrhy161YA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>


I encourage you to try ring modulation and see what kind of sounds you can produce just by using this effect, try using different waveshapes and see how you can produce complex spectra, like in the example below.

![ring-saw](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/RingModulation/Fig6_ring-saw.JPG){: width="605" height="660" }
_Fig.6 - Using a sawtooth as carrier_

![spectrum-saw](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/RingModulation/Fig7_saw-ring-spec.JPG){: width="776" height="232" }
_Fig.7 - More complex spectrum produced by ring modulation_

If you want to learn more about ring modulation check the references section: lots of great resources!


### References

Puckette, Miller. The theory and technique of electronic music. World Scientific Publishing Company, 2007.\
Strange, Allen. Electronic music: systems, techniques, and controls. William C Brown Pub, 1983.\
Aikin, Jim. Power tools for synthesizer programming: the ultimate reference for sound design. Backbeat Books, 2004.\
FLOSS Manuals <http://write.flossmanuals.net/pure-data/amplitude-modulation/>\
Wikipedia page <https://en.m.wikipedia.org/wiki/Ring_modulation>