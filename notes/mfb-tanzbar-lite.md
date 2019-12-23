# MFB Tanzbär Lite

## Description

MFB Tanzbär Lite is a drum machine with an internal step sequencer.

MFB Tanzbär Lite has 10 analog drum with tweakable and storable parameters. Each voice has its own individual potentiometers for levels, and there is also a master level (not programmable in memory).

MFB Tanzbär Lite's sequencer characteristics include:
* 64x patterns, in 4 banks of 16 patterns each.
* 11x tracks triggering the drum instruments
* 5x LFO for pitch modulation (bassdrum, clap, tom/conga, cowbell, and claves).
* 1-32 steps and 5 settings for scaling.
* A/b pattern toggle.
* Multiple triggering with roll/flam. 
* Chaining patterns, not programmable in memory.

## Power

* The power supply for this instrument has the following specs:

* 12 volt DC
* 500 mA
* center-positive

## Drivers and installation

MFB Tanzbär Lite needs no drivers or installation.

## Front panel

* 8x potentiometers for level:
  * BassDrum (BD)
  * SnareDrum (SD)
  * Claps (CP)
  * Tom/Conga (TC)
  * CowBell (CB)
  * Clave (CL)
  * Cymbal (CYM)
  * Hihat (HH)
* 19x potentiometers for sound parameters:
  * 3x Bass drum: decay, tune, tone
  * 3x Snare drum: decay, noise, tune
  * 3x Claps: filter, decay, attack
  * 2x Tom/Conga: decay, tune
  * 2x Cowbell: decay, tune
  * 2x Clave: decay, tune
  * 2x Cymbal: tone, decay
  * 2x Hihat: decay open hihat (OH), decay closed hihat
* 2x potentiometers for global parameters:
  * Master
  * Tempo
* 6x buttons for memory:
  * Snd (PLAY)
  * Select
  * Rec (REAL)
  * Patt (BNK)
  * A/B (CHAIN)
  * SHIFT
* 16x buttons for step sequencer:
  * BD (SHUFFLE)
  * BD-LFO (LAST STEP)
  * SD (SCALE)
  * RS (A/B TOGGLE)
  * CP (STORE PATTERN)
  * CP-LFO (CLEAR PATTERN)
  * TT (COPY A)
  * CO (COPY B)
  * TT/CO-LFO (DUMP PATT BNK)
  * CB (FLAM)
  * CB-LFO (MANUAL/STEP MODE)
  * CL (ACCENT 1)
  * CL-LFO (ACCENT 2)
  * CYM (ACCENT 3)
  * OH (ACCENT 4)
  * HH (SETUP)

The following two tables are included on the front panel:

Sound -- Step Button
RS  ---- Volume   ---  1 - 16
CP  ---- Impulse  ---  1 - 16
T/C ---- Panorama ---  1 -  3
CYM ---- Tune     ---  1 -  8
LFO ---- Speed    ---  1 -  8
LFO ---- Amount   ---  9 - 12
LFO ---- Wave     --- 13 - 16

Setup -- Step Button
1 - MIDI Learn       --- 
2 - MIDI Notes Tx    --- On/Off
3 - MIDI Ctrl Send   --- On/Off
4 - MIDI Clk Send    --- On/Off
5 - MIDI Clk Thru    --- On/Off
6 - MIDI Clk Receive --- On/Off
7 - Manual Trigger   --- Rec

## Back panel

MFB Tanzbär Lite back panel features: 

* Power jack, for 12 volt DC 500 mA center-positive power supply.
* On/off switch
* 5x 1/8 inch TS mono individual outputs for the drum voices:
  * Bass
  * Snare
  * Claps
  * Tom/Conga
  * Hihat
* MIDI IN jack, 5-pin DIN
* MIDI OUT jack, 5-pin DIN
* Master audio output, 1/4 inch TRS stereo jack.

## Audio routing

MFB Tanzbär Lite has one master audio output (1/4 inch TRS stereo jack), and 5 additional instrument outputs (1/8 inch mono jack), one each for bassdrum, snare. clap, tom/conga, and hihat.

Rimshot, cowbell, clave and cymbal are only available from the master output.

When plugging a cable into an instrument output, this instrument will be disconnected from the master output.

## MIDI specs

MIDI input receives MIDI clock, MIDI notes, MIDI controller data, and MIDI program change data.

MIDI output transmits note data of all tracks, MIDI clock, MIDI song position pointer data, and MIDI program change data.

Any incoming MIDI on the input is also output through the output.

## GUI operation

Most of Tanzbär Lite's buttons cover more than one single function. Depending on the selected mode, the function of the buttons will change.

The main purpose of the function buttons (left-hand side) is selecting the operation mode (Play or Record), selecting patterns and banks as well as starting and stopping the sequencer and toggling between the A/B parts of a pattern. These are dual-function keys (except the Select key).
The Step keys (lower row) are also dual- or even triple-function keys. Depending on the operation mode, they change their function. In Play mode, they mute tracks and control various playback functions (e.g. shuffle, pattern length, scale, and A/B toggle).
In Record mode, they are used to program the step sequencer. Apart from that, there is
an additional sound parameter hidden behind them which cannot be accessed directly via the sound controls. The Step keys are also required when it comes to storing, clearing, and copying patterns.
The Shift key (bottom left) accesses the „shift function“ resp. second function of the other keys. On the front panel, the shift functions are always labelled in a darker font so make sure you put your glasses on (or turn on the flood lights).
Depending on the dedicated function, the shift function works in two different ways:
When a shift function only has two settings (e.g. on/off), or when all available values can directly be accessed in the next lower level, simply hit the shift key and keep it depressed. Now hit the desired step key to toggle between the two possible settings or enter the desi- red value. For example, the start/stop function and the selection of the four Accent levels works just this way.

## Pattern management

To save the current pattern:
* if necessary hold SHIFT and press Patt/Bank key to change the current preset bank.
* Hold SHIFT press the button STEP 5 (STORE PATTERN). All 16 LEDs will start flashing.
* Release SHIFT.
* Press STEP key to save the current preset in the corresponding memory location.
* If necessary, press SHIFT any time to abort the store pattern function.

To clear the pattern:
* Hold SHIFT and press STEP 6 (CLEAR PATTERN) twice.

Patterns with more than 16 steps allow for erasing either their A or B section:
* Press PATT key to select the desired pattern action.
* Hold SHIFT and press STEP 6 (CLEAR PATTERN).

Sending pattern bank:
Using the SHIFT function you can send the current pattern bank to another MIDI device.
* Hold SHIFT and press STEP KEY 9 (DUMP PATT BANK).
* The LEDs of the step keys visualze the data upload progress.
* The LED of the corresponding pattern that is being transmitted is flashing.
* As soon as the data is completed, the function will exit automatically.

Receive pattern bank:
* As long as the sequencer is inactive, the instrument will always be ready to receive a pattern bank as SysSex datafile.
* The LEDs of the step keys will tell you about the progress of data transmission.

## MIDI implementation

MIDI controller assignment

MIDI_CC_BD_TONE     002
MIDI_CC_BD_DECAY    064
MIDI_CC_BD_TUNE     003

MIDI_CC_SD_TONE     011
MIDI_CC_SD_NOISE    013
MIDI_CC_SD_DECAY    067

MIDI_CC_CP_DECAY    075
MIDI_CC_CP_FILTER   018
MIDI_CC_CP_ATTACK   076
MIDI_CC_CP_TRIGGER  077

MIDI_CC_TT_TUNE     019
MIDI_CC_TT_DECAY    020

MIDI_CC_CO_DECAY    078
MIDI_CC_CO_TUNE     079

MIDI_CC_CO_PAN      082
MIDI_CC_TT_PAN      073

MIDI_CC_CB_TUNE     084
MIDI_CC_CB_DECAY    085

MIDI_CC_CL_DECAY    086
MIDI_CC_CL_TUNE     087

MIDI_CC_CY_DECAY    088
MIDI_CC_CY_TONE     092

MIDI_CC_CY_TUNE     089
MIDI_CC_OH_DECAY    090
MIDI_CC_HH_DECAY    091
