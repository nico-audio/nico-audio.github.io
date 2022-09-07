---
title: Easter egg - Making a Pd sound design tool
author: nico
date: 2020-08-19 13:25:00
categories: [Pure Data]
---


### Introduction

I was reading an article about the sound of Ghost of Tsushima and the amazing world created by the Sucker Punch sound team and something Josh Lord (Senior Sound Designer) said caught my attention. While talking about the UI/UX sounds he said a particular tool was very useful: he created a Max/MSP patch for processing the source, something like a "happy accidents" generator that had the ability of printing out something that happened while he was tweaking the sound. I thought it sounded like a really interesting and useful sound design tool so I decided to try making my own version of a Pd tool that would do something similar. I'm going to show you how it looks like and then we'll see a little about what is going on inside.

![easter-egg-pd](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig1_EasterEgg_patch.png){: width="1472" height="832" }
_Fig.1 - Easter egg_


> PATCHING WITH HEADPHONES IS DANGEROUS. PLEASE BE CAREFUL, **PATCH SAFELY!**
{: .prompt-warning }

### Easter egg demo

<div style="text-align: center;"><iframe width="560" height="315" src="https://www.youtube.com/embed/Gj6VqbLJr6I" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

The main things I needed for this project, the way I interpreted it, were:

1. a way to open my source file
2. a way to print out "x" seconds from buffer into a file
3. some fx to manipulate the source

### Pick your sample

As I mentioned, first I had to create a way to open my source file and store it into an array to work with it, I used [openpanel] and [soundfiler] for that. The left outlet of [soundfiler] will output the number of samples - you need to divide this number by your sample rate to get the original playback speed and feed it to [phasor].

![open-panel-ee](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig2_OpenPanel.png){: width="551" height="432" }
_Fig.2 - Opening your sample_

I used the phasor rate information and sent it to an HSlider to manipulate playback speed and added a bang to reset to original speed and another one to set it to 0. There is a tutorial by Dr.Rafael Hernandez (cheetomoskeeto) that teaches you something similar, definitely check it out if you are interested or not following this very well - I will add it to the references section.

![tabread-easter](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig3_tabread-easter.png){: width="488" height="384" }
_Fig.3 - Reading the table_

Now that you have set the phasor speed, multiply it by the sample size and read the table. I have an [outlet~] because this is a subpatch that we are going to access from the main patch window so I'm also graphing the controls to that window so everything looks organized and usable. We're also going to have a send for the dry signal so we can use it later on in the mixer.

![gui-openpanel](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig4_gui-openpanel.png){: width="302" height="276" }
_Fig.4 - Controls for audio source subpatch_

The array “original” is in the main patch so I can visualize the waveform.

![waveform-table](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig5_waveform-table.png){: width="302" height="276" }
_Fig.5 - Source waveform_

After this, I wanted to make an fx chain, so I could have different ways of modifying my sample. I added ring modulation, 2 delays, chorus, reverb, low pass filter and a noise generator. I might add other things to the chain, but for now this allows me to play around quite a bit. The order of effects can be changed in any way you want.

### FX Chain

The effects are not the main focus here so I won't be into a lot of the details, however, I will show you how I implemented them. All the effects are subpatches, so you will see an [inlet~] and [outlet~] on them so the audio passes through.

Here's how the two different delays work:

![delay-subpatch](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig6_delay-subpatch.png){: width="616" height="410" }
_Fig.6 - Delay subpatch_

![slapback-delay](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig7_slapback-delay.png){: width="476" height="385" }
_Fig.7 - Slapback delay_

For reverb I used [freeverb~], a Schroeder/Moorer reverb external that uses 8 comb filters. We have dry/wet and room size controls, those are freeverb~ messages. I've also added gain control and a meter so we have control over amplitude. For more details, chech the help patch on [freeverb~].

![reverb-subpatch](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig8_reverb-subpatch.png){: width="489" height="301" }
_Fig.8 - Using freeverb~_

The chorus is produced by reading 3 copies of the delay line at a slightly different pitch and phase than the other. In other words, we have an input and the signal is distributed in 2 ways: one goes directly to the output and a copy goes to the delay line, then I can create 3 different LFO's that will read from a single delay line. We also have a gain control in this patch.

![chorus-sub](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig9_chorus-sub.png){: width="625" height="416" }
_Fig.9 - Chorus subpatch_

Then I added a simple low-pass filter using [lop~] and set its initial cutoff value to 137.

![lpf-subpatch](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig10_lpf-subpatch.png){: width="572" height="455" }
_Fig. 10 - Low-pass filter subpatch_

And ring modulation multiplying the [inlet~] by a modulator [osc~].

![easter-ring](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig11_easter-ring.png){: width="360" height="356" }
_Fig.11 - Ring modulation_

### Output

At the end of the chain, we're going to have a mixer with a visual meter and the master output is sent to the final sample generator, which I'm calling "filer" for now. The mixer receives the dry signal and adds it to the wet signal that comes from the FX chain. [s~lvl] will send information about our master level to the meter and  [s~toFiler] sends the master to the sample generator.

![output-mixer](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig12_OutputMixer.png){: width="565" height="647" }
_Fig.12 - Output patch_


Finally, this is one of the most important parts of this patch, because it defines how I got the last seconds of audio that I wanted to catch. So I have an [inlet~] that receives signal from the end of the chain and then I have to delay the input by defining a delay line that will be read later before [writesf~]. I used a counter before [makefilename] so I could have an incremental file name: my audio files will look like this “easter-egg0.wav”, “easter-egg1.wav” and so on... Then, I need pd to work a few steps so I used the [trigger] object or as you can see in the patch, [t b b b a] and this helps with the operation order, remember that trigger outputs from right to left so it will: create the file, then read delay line, start recording, wait “x”  seconds and then stop.

![buttons-catch-done](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig13_receive-filer.png){: width="290" height="168" }
_Fig.13 - Receiving signal_

![catch-audio-sub](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig14_catch-audio-sub.png){: width="546" height="509" }
_Fig.14 - Subpatch to print out last 15 seconds of audio_

![catch-contrls](https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/_posts/img/EasterEgg/Fig15_catch-contrls.png){: width="449" height="504" }
_Fig.15 - Controls for the subpatch_

I had a lot of fun doing this and I believe it's very easy to adapt to whatever needs I have in the future. There is still room for a lot of improvements. If you wish to try and use the patch, please feel free to download it from my [github repository](https://github.com/nico-audio/pd-patches/tree/master/easter-egg). 

### References

Crafting Ghost of Tsushima's Tremendous Sound\ 
<https://www.asoundeffect.com/ghost-of-tsushima-sound/>

Freeverb~\ 
<https://puredata.info/downloads/freeverb>

Cheetomoskeeto tutorial\ 
<https://www.youtube.com/watch?v=boX0v54SqtU&list=PL12DC9A161D8DC5DC&index=24>

Easter egg github\ 
<https://github.com/nico-audio/pd-patches/tree/master/easter-egg>

