# guitarchords

ASCII guitar chords for console and Flipper Zero

## About this program

This program will be written in C so that it can be modified and added as a `.fap` for the [Flipper Zero](https://flipperzero.one/) later.

Basically, this program shows a list of Guitar Chords in the [ASCII tab](https://en.wikipedia.org/wiki/ASCII_tab) format, where chords are show, in standard tuning, vertically rather than horizontally.

```text
e |-----|
B |-----|
G |-----|
D |-----|
A |-----|
E |-----|
```

In this layout `e` is the **high e** narrow string and `E` is the **low E** thick string.

The guitars I use typically have a 10 gauge (0.010 inch or 0.254 mm) diameter `e` string up to a 46 gauge (0.046 inch or 1.1684 mm) diameter `E` string, though some acoustic guitars uses a 12 gauge (0.012 inch or 0.3048 mm) for `e` up to a 54 gauge (0.054 inch or 1.3716 mm) `E` string.  YMMV.

I'm not a luthier, and personally I'm still learning guitar myself. A couple of sources about guitar strings and their thickness can be looked up at these two links.

- Produce Like a Pro [Understanding Guitar String Gagues: What Gague is Best for Me?](https://producelikeapro.com/blog/guitar-string-gauges-guide/)
- Stringjoy [Guitar String Gauges in MM: A Helpful Guide](https://stringjoy.com/guitar-string-gauges-in-mm/)

If you paid attention in physics class, you'd know that guitar strings *vibrate* when you pluck them. A vibration in a string is a wave. Acoustic resonance causes a vibrating string to produce a sound with a constant frequency.  This frequency can be observed as a subjective psychoacoustical attribute of sound known as *pitch*.

Pitch may be quantified as a frequency, but remember pitch is subjective whereas frequency is objective.

A guitar string has a number of frequencies at which it will naturally vibrate. These natural frequencies are called **fundamental frequencies**. They alre also called naturals, fundamentals, and harmonics, depending on what book or data source you look up.

Suppose I have a Sire Larry Carlton S7 electric guitar which has a 25.5 inch (647.7 mm) scale. The scale in this case is the lenght from the nut on the neck down to the bridge of the guitar. Suppose I have a set of Ernie Ball Regular Slinky nickel wound electric guitar strings. The set consists of a 10, 13, 17, 26, 36, and 46 gauge set of strings. 

| Str. | Dia. (Gauge) | Dia. (inches) | Dia. (mm) |
|------|--------------|---------------|-----------|
| `e`  | 10           | 0.010         | 0.2540    |
| `B`  | 13           | 0.013         | 0.3302    |
| `G`  | 17           | 0.017         | 0.4318    |
| `D`  | 26           | 0.026         | 0.6604    |
| `A`  | 36           | 0.036         | 0.9144    |
| `E`  | 46           | 0.046         | 1.1684    |

In standard tuning, unfingered guitar strings are tuned to specific frquencies.  In this next table, we will show the strings with their typical numer value and their scientific pitch notation.

| Str. | Num. | Sci. Pitch    | Frequency (Hz) |
|------|------|---------------|----------------|
| `e`  | 1    | E<sub>4</sub> | 329.6276       |
| `B`  | 2    | B<sub>3</sub> | 246.9417       |
| `G`  | 3    | G<sub>3</sub> | 195.9977       |
| `D`  | 4    | D<sub>3</sub> | 146.8324       |
| `A`  | 5    | A<sub>2</sub> | 110.0000       |
| `E`  | 6    | E<sub>2</sub> |  82.4069       |

Notice how on the `A` string, the frequency value is a whole number (integer). This is because all `A` values are integers. If you hold down the `G` string in the second fret from the nut, that will play an A<sub>3</sub> note, which has a frequency of 220 Hz.  If you hold down the `e` string at the fifth fret, that will play the standard pitch A<sub>4</sub> note which has a frequency of 440 Hz.

Coincidentally, playing the `E` string held down at the fifth fret sshould made the same sound as the `A` string in open (unfingered) position. That is, it will play an A<sub>2</sub>.  This is how guitar chords can be played in more than one position.

My point with sharing all that information was that I wanted to demonstrate how to calculate the tension, linear density, and other variables. Eventually, I'll add that to this README file. 

Guitars are chorded string instruments, so it is natural to play them not just one note at a time but many notes at once. The combination of these notes is what are called **chords**.

The purpose of this app is to provide a handy list of guitar tabs that are easy to understand.

It should be noted though, that because the tabs in ASCII format are veritcal, barres (string positions where you use your finger to cover multipe strings at once) will be denoted with the consective fret numbers. For example, if you are playing a D Major 7th (Dmaj7) where you need to hold down the `G`, `B`, and `e` strings on the second fret (all with your index finger), it will be written as

```text
e |--2--|
B |--2--|
G |--2--|
D |--0--|
A |-----|
E |-----|
```

"Hold on there! What is that `0`? And what's it mean when a string doesn't have a number on it like the `A` and `E` strings? And what finger should I use?"

All of these are great questions!

Firstly, if a string does not have a number, you *should not* play it. In chord book, this is often marked with an `x` at the top of the nut, but in ASCII notation, we simply can denote nothing on that line such that it is not plaed. So in Dmaj7, we don't play `A` or `E`.

Secondly, **open strings**, or strings we *should* play are strings that are *unfingered*, that is you should not have your finger on it but you should play it. In horizontal notation, this is often marked with an `o` at the top of the nut, or with no symbol at all.

In chord books, the dots are recognized as fingers. In some books, numbers are used instead of fingers or in horizontal format, the finger numbers are up top where the nut is.

The fingers are denoted as follows

| Num. | Finger                  |
|------|-------------------------|
|  0   | open string (no finger) |
|  1   | index finger            |
|  2   | middle finger           |
|  3   | ring finger             |
|  4   | little finger           |

AVOID playing guitar with your thumb! As tempting as it is to use it, even to hold down the `E` string, DON'T.

I'm a bit divided on how I should denote which fingers to use on a chord. Assuming you pluck the sound board with your right hand, and fret with you left hand, the finger closest to the nut should be your index finger. Closer to `E`, you will either use your index or middle finger, espeically if you are using a chord where you need to have two fingers in the same fret.  For example, in D Dominant 7th (denoted as D7), you want your index finger to be on the `B` string in the first fret to play C<sub>4</sub>, your middle finger in the second fret on the `G` string to play A<sub>3</sub>, and your ring finger *also* in the second fret on the `e` string to playF#<sub>4</sub>. In addition, `D` is also played open.

The tab would look like

```text
e |--2--|
B |--1--|
G |--2--|
D |--0--|
A |-----|
E |-----|
```

The tab shows what *fret* to put your fingers on. It doesn't say *which* tab you should use.

I propose a solution to this problem.

My proposal is to put the fret number on top, and the finger number on the string.
Here is what our D7 looks like.

```text
   012345
e |--3---|
B |-1----|
G |--2---|
D |0-----|
A |------|
E |------|
```

And the Dmaj7 from earlier

```text
   012345
e |--1---|
B |--1---|
G |--1---|
D |0-----|
A |------|
E |------|
```

Notice we start the count at zero so that we can mark our open strings with a `0`. Two spaces over, our index finger (marked with `1`) is on `G`, `B`, and `e` in the second fret.

So what happens if we play three Dmaj7 and a D7? We can write it like this.

```text
   012345 012345 012345 012345
e |--1---|--1---|--1---|--3---|
B |--1---|--1---|--1---|-1----|
G |--1---|--1---|--1---|--2---|
D |0-----|0-----|0-----|0-----|
A |------|------|------|------|
E |------|------|------|------|
```

There are a few of downfalls with using "finger fret" tab notation:

1. Measure and note length are not denoted, which might not be a big deal considering whole notes might require some distortion on an electric guitar to play for more than a quarter note.
2. Using a non-monospace font. You SHOULD use a monospace font so you can count the number of hyphens.
3. You are using a monospace font, but it uses litgatures. (e.g. Nerd Fonts).
4. You are using a word processor (e.g. Microsoft Word) that combines hyphens. Dontdo that. Use a text editor like Neovim or Notepad++.
5. It does take a lot longer to type.  Those four chords I wrote a little while ago could have been written like the example below, but it wouldn't tell us *which fingers* we should use.

```text
e |-2-2-2-2-|
B |-2-2-2-1-|
G |-2-2-2-2-|
D |-0-0-0-0-|
A |---------|
E |---------|
```

That is why this program exists.

## User Story

As a musician, I want an application to help be a better guitar player, and I want it on a device that is small.

- I want a list of chords so that I know which strings to play and which frets I need to hold down.
- I want to see a chord by name so that I can know which notes to play.
- I want to see a chord tab so I know which fingers I should use and where to put them on my fretboard.
- I want to string together a set of chords to form a melody that I can easily remember
- I want to run this app on a computer so that I can see what chords, tabs, and notes to play.
- I want to run this app on a handheld device (in this case the Flipper Zero), so that I can see what chords, tabs, and notes to play in a portable form factor.

## TODO List

- [ ] Clean up this README to put some stuff in documentation.
- [ ] Continue gathering information about the various music notations used 
- [ ] Enter in all the known chords. Some chords might have more than one position.
- [ ] Allow the user to look up chords by their primary key signature.
- [ ] Allow the user to look up chords by their interval (e.g. major, minor, augmented, diminished, etc.)
- [ ] Allow the user to look up a list of "power chords"
- [ ] Allow the user to see a list of chords commonly used in various music genres.
- [ ] Allow the user to find chords that might use a diffent tuning (i.e. Dropped D where `E` is changed from E<sub>4</sub> to D<sub>4</sub>.)
- [ ] Allow the user the ability to see this information in a command terminal. (LIke all good programs, start in the CLI. Graphics later.)
- [ ] Allow the user the ability to see this information on a handheld device. (For the moment, Flipper Zero)
- [ ] Allow the user to view chords as scales. (Harmonics?)
- [ ] More math/physics stuff in the documentation.
- [ ] A dictionary of words and defintions. (Convert musician-speak into geek-speek or english.)

## Wish List

- [ ] A graphical version of this program
- [ ] A graphical version of this program on Flipper Zero. (Pixel art is hard on a high res screen. So, defintely do this later.)
- [ ] Allow the user to use this application on a Google or Samsung watch. (Something Android other than a phone.) This will likely be a separate project, especially since it needs to be written in a different programming language for a different platform.
- [ ] Features to make it with open-source Digital Audio Workstations (DAWs).
- [ ] MIDI support. (Where my [Synthesia](https://synthesiagame.com/) fans at?)
- [ ] A [Synesthesia](https://en.wikipedia.org/wiki/Synesthesia) mode. (A mode for folks who can SEE sounds!)
- [ ] Other accesiblity modes, especially for people deaf or hard or hearing or interested in music therapy. (I should probably consult someone about that latter part.)
- [ ] Baby mode.  You know those parents who think that making their fetus listen to Motzart will make them geniuses when it actually doesn't? I'm just going to add this mode to have it play HEAVY METAL so that I can get blamed for why they conceived a "demon baby". (LOL!)  (In case you didn't know, your baby will still be either as smart--or more than likely stupid--regardless if you have them listen to Bethoven or Black Sabbath. Also, it's your own damn fault if you encorage them to listen to "Baby Shark" instead of putting on Black Flag on a car trips.)
- [ ] Features to piss off the Recording Industry Association of America. Did you think RIAA only goes after people who were file-sharing in the late 1990s and early 2000s?  No, they (and some of their artists or producers) will go after you not just for *playing* their music without their permission, but also [playing any *chord or melody* that **sounds** similar to their own music](https://www.buzzfeed.com/williambarrios/musicians-who-were-sued-for-plagiarism), even if you didn't sample their music. Fortunately, [a couple of musicians algorithmicly generated ever possible melody and released them to public domain](https://www.vice.com/en/article/wxepzw/musicians-algorithmically-generate-every-possible-melody-release-them-to-public-domain). So, *hopefully*, no more frivilous lawsuits. See [All The Music](http://allthemusic.info/).

Anything else I miss? I'm open to suggestions. File an issue. We might make something happen.
