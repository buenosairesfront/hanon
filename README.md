**English** · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [日本語](README.ja.md) · [中文](README.zh.md) · [हिन्दी](README.hi.md)

# U-MA Hanon

All 60 exercises of *The Virtuoso Pianist* by Charles-Louis Hanon, in the browser: you see them on the staff, you see **both hands on the keyboard** with every finger numbered, you hear them at the tempo you choose and, with a MIDI keyboard, the app listens to you and analyses your take.

**▶ Open the app:** https://buenosairesfront.github.io/hanon/

Nothing to install. The interface is in Spanish.

## How it works

1. **Pick an exercise.** The 60 exercises are grouped into the book's three parts: **I · 1–20** preparatory (magenta), **II · 21–43** advanced (cyan) and **III · 44–60** virtuosity (yellow). Tap a number below the keyboard, or tap the big exercise number at the top to open the full 1–60 grid.
2. **Choose a variant** when the exercise has one: scales (39) and arpeggios (41) come in all 24 keys in the book's order (each major followed by its relative minor; minors in harmonic and melodic forms), chromatic scales (40) in 8 intervals and directions, repeated notes (45) in 6 fingerings, staccato thirds or sixths (48)…
3. **Read the score.** Two staves show the exercise: **↑ ascending** (cyan) and **↓ descending** (magenta). On a phone you switch between them with tabs.
4. **Watch your hands.** The keyboard is the centre of the app. Both hands are drawn over the keys with their palms, every finger shows its number (1 = thumb … 5 = little finger, each with its own colour), and a dashed outline marks **the next hand position**. Under the keyboard, a row per hand shows the finger order of the current group and lights up the note that is sounding.
5. **Play it.**
   - **▶ 2 passes** – a short demo: the first two and the last two groups, so you hear the shape quickly.
   - **↑ ascending** / **↓ descending** – only one direction.
   - **↑↓×2** – the whole exercise, twice.
   - **loop** repeats until you press **stop**.
6. **Set the tempo** from 40 to 160 BPM with the slider or the – / + buttons. The yellow band under it marks Hanon's own range (60 → 108): start slow and work up. The **MET** metronome blinks and clicks in the exercise's metre (2/4, 3/4, 4/4 or 6/8), accent in magenta.

## Practising with a MIDI keyboard

Press **MIDI** and allow access. From then on:

- the keys you press light up in cyan on the on-screen keyboard;
- **REC** plays the exercise as a guide and records what you play over it;
- when it ends you get an **analysis of your take**: accuracy (%), average deviation (ms), evenness (%) and wrong notes; a timing chart (early ↓ / late ↑ for every note), delay and strength per finger, and dynamics for each hand (right hand above, left below).

Without MIDI you can press **new example take** to see what the analysis looks like.

## Light and dark

The **light / dark** button changes the theme; your choice is remembered in that browser.

## Under the hood

A single `index.html` with no dependencies: the exercises are not stored as notes but **generated**. Each one is a melodic cell (in scale degrees) plus its fingering for each hand; the engine moves it up one degree per bar and back down, and spells every note correctly (sharps when ascending, flats when descending in the chromatic ones). Scales, arpeggios and octave exercises are built for each of the 24 keys with the traditional fingerings. The score is drawn in SVG, the keyboard and the analysis on `<canvas>`, sound and metronome with Web Audio, and the keyboard input with Web MIDI.

## Run locally

Download `index.html` and open it, or serve the folder:

```
python3 -m http.server 8000
```

<!-- u-ma:more -->
**More from U-MA:** every instrument and tool in one place → [U-MA showcase](https://github.com/buenosairesfront/U-ma)
<!-- /u-ma:more -->

## Credits

Exercises from *Le Pianiste virtuose en 60 exercices* by Charles-Louis Hanon (1873, public domain). App by U-MA サウンド · [Buenos Aires Front](https://www.instagram.com/buenos.aires.front/).
