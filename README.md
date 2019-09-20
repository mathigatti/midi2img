# MIDI to Image conversion

## Implementation Details
This script relies on the music21 library to parse and create MIDI files. The expected images are black and white and have a fixed size of 106 rows and 100 columns. 106 is the number of different notes (From 21 (`A0`) to 127 (`G9`)) and 100 is the length of the song, if a song is longer than that the script splits the song and generates several images. Each image represents one instrument, if a song has several instruments different images are generated for each. Each pixel represents a note played for 1/4 beats, this can be changed with the `resolution` variable.

## Demo
[Here](https://www.youtube.com/watch?v=YJ-TEpLwuns) is a video demonstration using the program to generate midis and images, then we use it for an artistic performance.

[![IMAGE ALT TEXT HERE](https://i.ytimg.com/vi/YJ-TEpLwuns/maxresdefault.jpg)](https://www.youtube.com/watch?v=YJ-TEpLwuns)

## Requirements
- python 3
- python libraries (Try something like: `pip install music21`)
  - music21
  - imageio
  - numpy
  - PIL (Pillow)

## Usage
There are two scripts, one for converting a MIDI into images and the other one to convert an image into a MIDI.

### MIDI to Image

REPETITIONS parameter indicates in case the song is too long how many parts of the song to convert into an image. If it is 1 it only extracts the first part of the song.

```
python midi2img.py MIDI_FILE_PATH REPETITIONS
python midi2img.py samples/zelda.mid 1
```

Using the sample zelda midi the generated image for the first part of the song looks like this
<div style="text-align:center">
<img src="samples/converted_samples/zelda_Piano_0.png" width="400" height="400" />
</div>

### Image to MIDI

Converts image of size (106,100) into a midi file.

```
python img2midi.py IMAGE_PATH
python img2midi.py samples/image.png
```

Using the image from the sample folder it generates as expected a midi file with decreasing and increasing notes.
<div style="text-align:center">
<img src="samples/image.png" width="400" height="400" />
</div>

