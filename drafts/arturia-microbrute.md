# Arturia MicroBrute

## Installation

## Power  

## Jacks, switches and knobs

### Front panel

### Back panel

* Finetune: knob
* CV GATE Pitch Out / Key Follow + Pitch Bend: jack
* CV GATE Gate Out: 1/8" mono output jack
* CV GATE Gate In: 1/8" mono output jack
* AUDIO Line Out: 1/4" mono output jack
* AUDIO Headphones: 1/8" stereo output jack
* AUDIO Input Level: knob
* AUDIO Input: 1/4" mono input jack
* MIDI IN: MIDI DIN -5 jack
* USB: USB-B jack
* 12V DC 1A: power jack, center-positive
* Power: switch for turning on/off

## Overview


## Playing sounds  


## Editing the sound


## Factory Reset

## System Settings  

## MIDI implementation chart

|Function                      |Transmitted|Recognized|Remarks                 |
|------------------------------|-----------|----------|------------------------|
|Basic Channel Default         |1          |1         |Memorized               |
|Basic Channel Changed         |1-16, off  |1-16, off |                        |
|Mode Default                  |Mode 3     |Mode 3    |                        |
|Mode Messages                 |x          |x         |                        |
|Mode Altered                  |********** |**********|                        |
|Note Number:                  |*1         |*2        |                        |
|Note Number: True voice       |********** |          |                        |
|Velocity: Note On             |o 9nH v=80 |o         |                        |
|Velocity: Note Off            |o 8nH v=00 |o         |                        |
|After Touch Key's             |x          |x         |                        |
|After Touch Channel's         |x          |x         |                        |
|Pitch Bend                    |x          |x         |                        |
|Control Change  9             |x          |o         |SHUFFLE                 |
|Control Change 20             |o          |o         |BD TUNE                 |
|Control Change 21             |o          |o         |BD ATTACK               |
|Control Change 22             |o          |o         |BD COMP                 |
|Control Change 23             |o          |o         |BD DECAY                |
|Control Change 24             |o          |o         |BD LEVEL                |
|Control Change 25             |o          |o         |SD TUNE                 |
|Control Change 26             |o          |o         |SD SNAPPY               |
|Control Change 27             |o          |o         |SD COMP                 |
|Control Change 28             |o          |o         |SD TONE                 |
|Control Change 29             |o          |o         |SD LEVEL                |
|Control Change 46             |o          |o         |LT TUNE                 |
|Control Change 47             |o          |o         |LT DECAY                |
|Control Change 48             |o          |o         |LT LEVEL                |
|Control Change 49             |o          |o         |MT TUNE                 |
|Control Change 50             |o          |o         |MT DECAY                |
|Control Change 51             |o          |o         |MT LEVEL                |
|Control Change 52             |o          |o         |HT TUNE                 |
|Control Change 53             |o          |o         |HT DECAY                |
|Control Change 54             |o          |o         |HT LEVEL                |
|Control Change 55             |o          |o         |RS TUNE                 |
|Control Change 56             |o          |o         |RS DECAY                |
|Control Change 57             |o          |o         |RS LEVEL                |
|Control Change 58             |o          |o         |HC TUNE                 |
|Control Change 59             |o          |o         |HC DECAY                |
|Control Change 60             |o          |o         |HC LEVEL                |
|Control Change 61             |o          |o         |CH TUNE                 |
|Control Change 62             |o          |o         |CH DECAY                |
|Control Change 63             |o          |o         |CH LEVEL                |
|Control Change 71             |o          |o         |TOTAL ACCENT            |
|Control Change 80             |o          |o         |OH TUNE                 |
|Control Change 81             |o          |o         |OH DECAY                |
|Control Change 82             |o          |o         |OH LEVEL                |
|Control Change 83             |o          |o         |CC TUNE                 |
|Control Change 84             |o          |o         |CC DECAY                |
|Control Change 85             |o          |o         |CC LEVEL                |
|Control Change 86             |o          |o         |RC TUNE                 |
|Control Change 87             |o          |o         |RC DECAY                |
|Control Change 88             |o          |o         |RC LEVEL                |
|Program Change                |x          |x         |                        |
|Program Change: True Number   |********** |**********|                        |
|System Exclusive              |x          |x         |                        |
|System Common: Song Position  |o          |o         |                        |
|System Common: Song Select    |o 0-7      |o 0-7     |                        |
|System Common: Tune Request   |x          |x         |                        |
|System Real Time: Clock       |o          |o         |                        |
|System Real Time: Start       |o          |o         |                        |
|System Real Time: Continue    |o          |o         |                        |
|System Real Time: Stop        |o          |o         |                        |
|Aux Msg: All Sound Off        |o          |o         |Transmitted:MIDI OFFLINE|
|Aux Msg: Reset All Controllers|o          |o         |Transmitted:MIDI OFFLINE|
|Aux Msg: Local On/Fff         |x          |x         |                        |
|Aux Msg: All notes Off        |o          |o         |Transmitted:MIDI OFFLINE|
|Aux Msg: Omni Mode Off        |x          |o         |*3                      |
|Aux Msg: Omni Mode On         |x          |o         |*3                      |
|Aux Msg: Mono Mode On         |x          |o         |*3                      |
|Aux Msg: Poly Mode On         |x          |o         |*3                      |
|Aux Msg: Active Sensing       |o          |o         |                        |
|Aux Msg: System Reset         |x          |x         |                        |

Notes:
* 3: Same process as All Notes Off



Modes:
* 1: OMNI ON, POLY
* 2: OMNI ON, MONO
* 3: OMNI OFF, POLY
* 4: OMNI OFF, MONO

Signs:
* o: Yes
* x: No

* 1:

|Instrument   |Note Number|
|-------------|-----------|
|BASS DRUM    |36         |
|SNARE DRUM   |38         |
|LOW TOM      |43         |
|MID TOM      |47         |
|HIGH TOM     |50         |
|RIM SHOT     |37         |
|HAND CLAP    |39         |
|CLOSED HI-HAT|42         |
|OPEN HI-HAT  |46         |
|CRASH CYMBAL |49         |
|RIDE CYMBAL  |51         |


* 2:

|Instrument   |Note Number|
|-------------|-----------|
|BASS DRUM    |35, 36     |
|SNARE DRUM   |38, 40     |
|LOW TOM      |41, 43     |
|MID TOM      |45, 47     |
|HIGH TOM     |48, 50     |
|RIM SHOT     |37         |
|HAND CLAP    |39         |
|CLOSED HI-HAT|42, 44     |
|OPEN HI-HAT  |46         |
|CRASH CYMBAL |49         |
|RIDE CYMBAL  |51         |
