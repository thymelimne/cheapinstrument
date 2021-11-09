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

<h2>Challenge to keep in mind: Tuning the virtual instrument.</h2>
Most pianos nowadays are tuned with something called "equal temperament" -- That is, with each note having a regular mathematical relationship with the next note. Figuring out the frequency of any note on a piano tuned to equal temparement is simple:

<br>Middle A is usually 440Hz, though this isn't quite as important as the next statement...<br>
<br>Frequency of a new note = 2 ^ ((amount of notes upward from the original note) / 12)<br>

<br>However, there are other tuning methods as well. There's well temperament, in which the note frequencies are slightly irregularly altered from equal temperament, so as to make certain specific major thirds ring out more nicely. There's also pythagorean tuning, and other tuning methods as well.<br>

<br>This project might end up using an array as an imaginary tuned piano; It'll calculate the frequencies at the beginning of the program's runtime, according to which tuning rules are desired for this runtime, and then as each note gets played, the program will use this table to look them up. This would hopefully accomplish two things: Firstly, it'll hopefully pare down runtime by not requiring the frequency calculation be done for each note. Secondly, it would make it very easy to construct new tuning systems in the future, by adding modifications to an array as opposed to coming up with mathematical rules to code into new functions.

<h2>NES sounds</h2>
The way sound channels worked on the NES game console and the Commodore 64 gaming computer are fairly interesting. There may come more explanation here on how it worked, if it's found to be relevant enough to this project... 
