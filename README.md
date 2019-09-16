# MIDI to Image conversion

This script relies on the sinsy.jp website from the Nagoya Institute of Technology which implements a HMM-based Singing Voice Synthesis System.

You can find a sample merged with the instrumental audio [here](https://soundcloud.com/mathias-gatti/somebody-that-i-used-to-know-sinsy-synthetic-voice).

## Requirements
- python 3
- python libraries (Try something like: `pip install music21`)
  - music21
  - imageio
  - numpy
  - imageio
  - PIL (Pillow)

## Usage
It is used running the main script `midi2voice.py`, it has four parameters, the lyrics_file, midi_file, singer sex (optional) and tempo (optional).

### MIDI to Image

```
python midi2img.py samples/zelda.mid 1
```

### Image to MIDI

```
python img2midi.py samples/image.png
```
