# cheapinstrument
CheapInstrument: a desktop application made with the hopes of making music production easier and simpler, regardless of the creator's access to instruments or special hardware.

The goal is to make it easy for a user to play desired chords in real-time, and define their sounds in particular ways.

There is some work ahead to make this code organized the right way.

<h2>TO GET: a music theory library</h2>
There are certain music theory concepts that will be referred to often, and all parts of this code should have a shared, simple way to refer to them. For this reason, the current plan is to either find or make a library of music theory concepts. This library should contain classes that may abstractly represent the following things:

<h3>Baseline concept: notes</h3>
Chords are made up of notes, so notes should be built before chords are built. For this project, this app's idea of a "note" should mark the following concepts:
<br>
<br>
<ul>
  <li>The twelve tones of a common musical scale, and the cyclical nature</li>
  <li>The common tuning for the standard Western twelve-tone scale (middle C is usually ~621.63Hz)</li>
  <li>The relationship between notes in a twelve-tone scale, with regards to the variation in frequency (frequency, a.k.a. pitch)</li>
  <li>The octave of each note</li>
  <li>NOT to be represented in this area of code: ...The waveform of a note -- this library won't be concerned with that.</li>
  <li>NOT to be represented in this area of code: ...To be implemented later down the line, but a by-the-measure time layout of notes could be helpful at some point. This could include time signatures, tempo, and notes contained in each time measure. Additional bells and whistles could be fermata, ritardando, accelerando, etc.</li>
  <li>NOT to be represented in this area of code: ...As an optional attribute for a note, approximate loudness could be represented: ppp, pp, p, mp, m, mf, f, ff, fff. Combining this concept with the previous bullet point, crescendos and decrescendos could be implemented.</li>
  <li>TRY TO ALLOW FOR: 
</ul>
<h3>Building up: chords</h3>
The goal of the app is to play chords, so a chord should represent the following:
<br>
<br>
<ul>
  <li>Root note of the chord (root note, a.k.a. 'tonic', or 'base')</li>
  <li>Whether the chord is major, minor, aug, dim, etc.. a.k.a, the chord's 'quality'.</li>
</ul>
