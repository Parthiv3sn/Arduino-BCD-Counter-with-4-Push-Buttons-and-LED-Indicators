# Arduino BCD Counter with Push-Button Input

An Arduino sketch that reads four buttons as a binary-coded decimal (BCD) input and displays the resulting value (0–15) on a single common-cathode seven-segment display.

## Features

- Four active-low button inputs
- Binary value assembled from button states
- Single-digit seven-segment output using the SevSeg library

## Hardware

- Arduino Uno or compatible board
- Common-cathode seven-segment display
- 4 momentary push-buttons

## Wiring

| Function | Arduino pin |
| --- | --- |
| Segment pins a–g | 2–8 |
| Button bits 0–3 | 9–12 |

Buttons use `INPUT_PULLUP`; wire each one between its input pin and GND.

## Setup

1. Install the **SevSeg** library.
2. Open `Source Code` (rename it to `BCDCounter.ino` if needed).
3. Verify the seven-segment pin ordering matches `SegPins`.
4. Upload the sketch.

## Important note

The sketch now includes the missing closing brace for `setup()`, which previously prevented compilation. The display configuration still needs to match the actual wiring; verify the common and segment pins before upload.

## Project files

- `Source Code` — Arduino sketch
- `Circuit.image .png` — wiring reference

## Improvement ideas

- Add software debouncing and an explicit binary-value indicator.
- Support multi-digit display output for values above 9.
- Use named constants and a wiring diagram with segment labels.

## License

No license has been specified. Add one before reusing or distributing this work.