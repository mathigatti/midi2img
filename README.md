# MIDI to Image conversion

This script relies on the music21 library to parse and create MIDI files. The expected images have a fixed size of 106 rows and 100 columns. 106 is the number of different notes (From 21 (`A0`) to 127 (`G9`)) and 100 is the length of the song, if a song is longer than that the script splits the song and generates several images. Each image represents one instrument, if a song has several instruments different images are generated for each.

## Requirements
- python 3
- python libraries (Try something like: `pip install music21`)
  - music21
  - imageio
  - numpy
  - imageio
  - PIL (Pillow)

## Usage
There are two scripts one for converting a MIDI to images and the other one to convert an IMAGE into a MIDI.

### MIDI to Image

REPETITIONS parameter indicates in case the song is too long how many parts of the song to convert into an image. If it is 1 it only extracts the first part of the song.

```
python midi2img.py MIDI_FILE_PATH REPETITIONS
python midi2img.py samples/zelda.mid 1
```

Using the sample zelda midi the generated image for the first part of the song looks like this

<img src="samples/converted_samples/zelda_Piano_0.png" alt="drawing" width="400", height="400"/>

### Image to MIDI

Converts image of size (106,100) into a midi file.

```
python img2midi.py IMAGE_PATH
python img2midi.py samples/image.png
```
