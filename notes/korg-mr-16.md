# KORG MR-16 MIDI RHYTHM SOUND UNIT

## Description

KORG MR-16 is a drum machine.

This instrument uses PCM digital samples for its 19 drum and percussion sounds, plus its 2 metronome sounds, for a total of 21 sounds:

1. Bass drum (BD)
2. Rimshot (RS)
3. Snare drum (SD)
4. Handclaps (CP)
5. Low tom (LT)
6. High tom (HT)
7. Closed hi-hat (CHH)
8. Open hi-hat (OHH)
9. Crash cymbal (CR)
10. Ride cymbal (RD)
11. Low conga (LC)
12. High conga (HC)
13. Tambourine (TA)
14. Cowbell (CB)
15. Timbale (TI)
16. Cabasa (CA)
17. Wood block (WB)
18. Low agogo (LA)
19. High agogo (HA)
20. Metronome piano (MP)
21. Metronome forte (MF)

The KORG MR-16 groups its drum and percussion soundss (except for metronomes) in 16 drum voices, each one with their dedicated volume knob, panning knob, and separate output. All sounds get their own drum voice, except for:

* SNARE / RIM: snare drum and rimshot
* HI HAT: open hi-hat and closed hi-hat
* COWBELL / WOOD BLOCK: cowbell and wood block

These are the 16 resulting drum voices:

1. BASS DRUM (BD)
2. SNARE / RIM (SD / RS)
3. LOW TOM (LT)
4. HI TOM (HT)
5. HI HAT (CHH / OHH)
6. CRASH CYMBAL (CR)
7. RIDE CYMBAL (RD)
8. HAND CLAPS (CP)
9. LOW CONGA (LC)
10. HI CONGA (HC)
11. TIMBALE (TI)
12. TAMBOURINE (TA)
13. COWBELL / WOOD BLOCK (CB / WB)
14. CABASA (CA)
15. LOW AGOGO (LA)
16. HI AGOGO (HA)

## Power

KORG MR-16 can be powered with the same power supply as most stompboxes, as in: 
* 9 volt DC
* Center negative polarity

An example of power supply is the Truetone 1 Spot.

## Drivers and installation

KORG MR-16 has no drivers.

## Front panel

* 1 master knob, 0-10, 0 turns off the KORG MR-16.
* 16 volume knobs (VOL), one for each drum voice.
* 16 panning knobs (PAN), one for each drum voice.
 
## Back panel

* Power supply input, 9 volt DC
* 2 audio outputs: R and L/MONO.
* 2 MIDI DIN jacks: IN and THRU.
* 6 DIP switches (FUNCTION SW):
  * 1 for METRONOME OFF(0)/ON(1)
  * 1 for BEATS/MEAS 3/4 (0) or 4/4 (1)
  * 4 for MIDI RCV CH, sets MIDI input channel, 1 (0000) to 15 (1111)
* 16 SEPARATE OUTPUTS, 1 for each drum voice.

## MIDI mapping

List of drum sound and decimal MIDI note number:

1. Bass drum (BD): 35, 36
2. Rimshot (RS): 37
3. Snare drum (SD): 38, 40
4. Handclaps (CP): 39
5. Low tom (LT): 41, 43, 45
6. High tom (HT): 47, 48, 60
7. Closed hi-hat (CHH): 42, 44
8. Open hi-hat (OHH): 46
9. Crash cymbal (CR): 49
10. Ride cymbal (RD): 51
11. Low conga (LC): 52
12. High conga (HC): 53, 55
13. Tambourine (TA): 54
14. Cowbell (CB): 56
15. Timbale (TI): 57, 59
16. Cabasa (CA): 58
17. Wood block (WB): 60, 62
18. Low agogo (LA): 61
19. High agogo (HA): 63
20. Metronome piano (MP): 64
21. Metronome forte (MF): 65

List of MIDI note number and drum sound:

35: BD bass drum
36: BD bass drum
37: RS rimshot
38: SD snare drum
39: CP handclaps
40: SD snare drum
41: LT low tom
42: CHH closed hi-hat
43: LT low tom
44: CHH closed hi-hat
45: LT low tom
46: OHH open hi-hat
47: HT high tom
48: HT high tom
49: CR crash cymbal
50: HT high tom
51: RD ride cymbal
52: LC low conga
53: HC high conga
54: TA tambourine
55: HC high conga
56: CB cowbell
57: TI timbale
58: CA cabasa
59: TI timbale
60: WB woodblock
61: LA low agogo
62: WB woodblock
63: HA high agogo
64: MP metronome piano
65: MF metronome forte

## Accents

MIDI velocity data can be used to accent particular sounds. There are two volume levels:

Velocity data:
* 0: no sound
* 1 to 95: normal volume
* 96 to 127: accented sound

## Volume control

There are 3 ways to control the volume of the sound output through the OUTPUT jacks (R and L/MONO):

1. Fron panel volume controls for each sound.
2. MIDI control change data for total volume control.
3. Fron panel master volume control.

MIDI control change #7 is used when changing volume, other CC numbers are ignored.

THe SEPARATE OUTPUT jacks on the back panel have fixed levels, except for controlled accents. 

## MIDI SPECS

1001nnnn 0kkkkkkk 0vvvvvvv - note on (NOTE 1)
1001nnnn 0kkkkkkk 00000000 - note off (NOTE 2)
1011nnnn 00000111 0vvvvvvv - volume control (NOTE 3)

11111000 - timing clock (F8) (NOTE 4)
11111010 - START (FA)
11111011 - STOP (FC)
11111011 - CONTINUE START (FB)

NOTES:

1. A sound is accented when its velocity value is 96 or higher.
2. if NOTE OFF, MR-16 will not stop sound outputs.
3. Volume control resolution is 7-bit, with the least significant bit ignored.
4. The timing clock data can be received in the interval between a start message and a stop message.
