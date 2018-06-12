# maquinitas

## notes on bastl microgranny 2

## midi channel

microGranny 2 has midi input.

to set the midi channnel, hold down one of the big buttons while turning on the microgranny, to set the input channel to 1-6. by doing the same procedure wihle the FN button is pressed, you set the input channel to 7-12.

the input channel is indicated on the display each time you turn on the microgranny, for example "CH 2" for MIDI input channel 2.

## MIDI notes

microGranny reads note messages and reacts to velocity. the first 6 notes of the lowest MIDI octave corresponding to the 6 buttons on the microgranny.

if the TUNED parameter is turned ON, the last played sound gets spread and transposed on the keyboard in the range of 3 and a half octaves. The middle C note is the original pitch of the sample (C4, note number 60). The transposed mode is active from 3 octaves below this note (C1 - note number 24) to 6 semitones above this note (F4 - note number 64).

If the TUNED parameter is turned OFF, the range of 5 octaves (with C4 in the middle) represents the whole sample and pressing different keys sets starting position of the playback. When used with granular settings this feature can be used to play individual grains.

Tip: in case you happen to have some hanging MIDI notes, turning ON and OFF the HOLD function will reset the MIDI note buffer.

## MIDI CC

microGranny reacts to MIDI CC messages to set the parameters of the sound, CC mapping is 102 = SAMPLE RATE, 103 = CRUSH, 104 = ATTACK, 105 = RELEASE, 106 = GRAIN SIZE, 107 = SHIFT SPEED, 108 = START, 109 = END, 0 = PRESET CHANGE. Modulation wheel sets the GRAIN SIZE and Sustain pedal is also, too.

## MIDI Sync

## MIDI out / thru and chaining
