# Parabolic Flight 0G Simulation

An interactive physics simulation of a zero-g parabolic flight manoeuvre, made for a presentation about my flight during the **ESA 90th Parabolic Flight Campaign**.

**Live demo:** https://maciekspy.github.io/flight-0g-sim/

## What it shows

The page plays one full parabola, phase by phase: level flight → pull-up (~1.8 g) → weightlessness (0 g) → pull-out (~1.8 g) → level flight. Four views stay in sync:

- **Trajectory**: the aircraft's flight path, coloured by phase (the vertical scale is exaggerated).
- **Forces on the aircraft**: a free-body diagram with lift, weight, thrust, drag and the net force.
- **Cabin**: what passengers feel. A person and a ball respond to the floor force and float freely during 0 g.
- **Load factor and altitude over time**: a chart of *n* and *h* across the manoeuvre.

A stats bar shows time, altitude, speed, flight-path angle, load factor and vertical speed.

## Physics model

It uses a point-mass model of an A310-class aircraft (~140 t). Lift acts perpendicular to the flight path, and thrust and drag act along it. The main parameters are at the top of the script in `index.html`:

| Parameter | Value |
|---|---|
| Mass | 140 000 kg |
| Initial speed / altitude | 200 m/s / 6000 m |
| Lift-to-drag ratio | 16 |
| Pull-up / pull-out load factor | 1.8 g |
| Path angle at parabola entry / exit | 45° / 42° |

## Usage

The project is a single, self-contained `index.html` with no build step and no dependencies. Open it in a browser or use the live demo.

- **Space**: play / pause
- **← / →**: step 0.5 s (hold **Shift** to step 5 s)
- Playback speed runs from 0.25× to 8×.
- Language: English or Polish. To add another language, add an entry to the `I18N` object.
