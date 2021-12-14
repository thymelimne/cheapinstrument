# cheapinstrument
CheapInstrument: a desktop application made with the hopes of making music production easier and simpler, regardless of the creator's access to instruments or special hardware.

The goal is to make it easy for a user to play desired chords in real-time, and define their sounds in particular ways.

There is some work ahead to make this code organized the right way.

<h2>Sound production</h2>
This is being made as a C++ application on a Windows machine. In order to get a start producing sounds, this project will be building off of a simple C++ synthesizer by GitHub account OneLoneCoder: https://github.com/OneLoneCoder/synth
. This synthesizer has enough implemented to enable the user to play certain notes and have them sound out by the machine. This is extremely helpful as a jumping-off point, but there are plans to restructure some code for this project to allow for certain features:

<h4>---> Envelope data structure, that doesn't just adhere to the ADSR standard</h4>
See the README for the byoi-cheapinstrument repository for more explanation.

<h2>Representing chords</h2>
Chord notations can be represented with a single integer - Cuius rei demonstrationem mirabilem sane detexi; hanc marginis exiguitas non caperet...

<h2>Additive vs. Subtractive Synthesis</h2>
As it seems, the goal of music synthesis is to create a sound output. Let's visualize this as a single squiggle: the wave of sound that changes itself along the duration of playtime.
![image](https://user-images.githubusercontent.com/91765107/145726739-2ad5d316-e2ea-4f9f-a1fc-9b6e951899c0.png)
...
 <br><br>It seems that a synth that employs additive synthesis is one that builds all its waves by compounding multiple sine different sine waves together. This gives you a comprehensive set of sounds you can make, but means that you need multiple sine wave channels, the more the better, to make these compound sounds. For this reason, additive synthesis is a concept more associated with software-based synthesizers than older/hardware-based ones, because a programmer has more ease and RAM to define multiple sound channels than the hardware engineer, who would have to physically build and connect those multiple sound channels with physical cables.

Subtractive synthesis is where, instead of compounding enough sine waves to create whatever waveform you want, you have a few different types of waves (triangle wave, pulse wave, saw wave -- waveforms that themselves are already mathematically defined as compounds of sine waves, but are commonly hard-programmed into your synthesizer or computer sound card) that you generate, and then modify using a harmonic filter. Sound engineers generally agree that the filter is where the individual intrigue of the sound's timbre usually lies, because it offers so much variety of sound.

For this project, there's a conceptual question that requires some studying: How do filters actually work? The idea of how they interface with 
