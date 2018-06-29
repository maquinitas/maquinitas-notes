# BASTL microGranny 2


## Power

The microGranny can be powered with a 9 volt battery or with a 9 volt DC center-positive power supply.

## Jacks, switches and knobs

### Front panel

* G - SAMPLE RATE / B - GRAIN SIZE: knob
* G - CRUSH / B - SHIFT SPEED: knob
* G - ATTACK / B - START: : knob
* G - RELEASE / B: END: knob
* INPUT: knob
* OUTPUT: knob
* MIC: microphone
* RGB LED: lights up red for recording mode, and green or blue for G and B pages
* RECORD / SAVE: round red button
* PAGE / PRESET: round black button
* FN: round black button
* UP / COPY: triangle black button
* DOWN / PASTE: triangle black button
* HOLD / INSTANT LOOP: round black button
* TUNED: square black button
* LEGATO: square black button
* REPEAT: square black button
* SYNC: square black button
* RANDOM SHIFT: square black button
* RNDMZR: square black button

### Back panel

* INPUT: jack
* OUTPUT: jack
* MIDI: DIN jack for MIDI in
* BATT-PLUG: switch for choosing power supply
* SD: slot for micro SD card
* 9V (-) ( (+): jack for power supply

## Playback and hold

Press the big square black buttons to hear the sounds. the last pressed button will play the sound.

Pressing the HOLD button, the HOLD mode is activated, indicated by the HOLD LED. Now you don't have to hold down the buttons in order to keep them playing. If you press an already playing button, it will start from the beginning. To stop playback press the HOLD button again.

## Sample selection

Play one of the 6 sounds. By pressing the UP or DOWN button you can select samples that are stored on the SD card. The name of the sample is indicated on the display. By holding UP or DOWN longer than 2 seconds, the first letter of the sample begins to change, which allows faster browsing of the directory. If it's searching, the display will say SRCH.

## Knobs  

The 4 knobs on the left side adjust the parameters of the sound. The actual function of the knobs is dependent on the PAGE which is indicated by the color of the RGB LED. Whether a knob is active or not is indicated by the LEDs next to each knob. In order to activate the knob, the knob has to reach the original value. You have to turn it, to match the original value. The 2 knobs on the right side of the microGranny adjust input and output volume.  

## FN button

The FN button allows access to more functions and parameters. Hold down the FN button and press the big square black buttons to change parameters of the last played sound: TUNED, LEGATO, REPEAT, SYNC, and RANDOM SHIFT. The state of these parameters is indicated by the LEDs while the FN button is pressed. Hit the last big button to play a DEMO.

By pressing the UP or DOWN button in combination with the FN button, you can do COPY and PASTE respectively. The last played sound is copied by the COPY function. To the last played sound, the copied sound will be pasted by the PASTE function.

When a sound is playing you can press the HOLD button in combination with the FN button to call the INSTANT LOOP function. The first call of the INSTANT LOOP marks the start of a loop, the second press marks the end and loops in between these points (indicated by "LOOP" on the display), and a third press deactivates the INSTANT LOOP.

By pressing the RECORD button in combination with the FN button you SAVE the current PRESET.

## Parameters of the sound

SAMPLE RATE is the pitch of the played sound. It can operate in two different mods, depending on the sound's TUNED parameter. Initially the TUNED parameter is turned on, which means that the SAMPLE RATE is changed in semitones in a range from -36 to 5, where 0 is the original pitch. When TUNED is turned off, the SAMPLE RATE can be adjusted in a fine resolution from -360 to 50, which is 10 times higher and corresponds to the tuning (when TUNED is turned on -12 is the same pitch as -120 when turned off).

CRUSH is the distortion effect applied to the sound.

START marks the playback starting position. The sample gets chopped into 1024 points and START selects the starting point. When START is set to 0 it means the sample is played from the beginning.

END marks the playback ending position. Again it is one of 1024 points of the file. When END is set to maximum it means the whole sample is played. Note: ending position cannot be set lower than the starting position.

GRAIN SIZE sets the size of the GRAIN loop. When GRAIN SIZE is set to 0 there is no granular effect applied to the sound and therefore the SHIFT SPEED function doesn't affect the sound either.

SHIFT SPEED sets the speed at which the GRAIN loop travels through the sample. It ranges from -127 to 128, where 0 means the GRAIN loop is static. The negative numbers mean that the GRAIN loop travels backwards (from the end position to the start position).

ATTACK sets the volume envelope attack. This means how long it takes for the sound to fade from silence to the maximum volume.  

RELEASE sets the volume envelope release. This means how long it takes for the sound to fade to silence, after the playback of the sound was stopped.

TUNED see SAMPLE RATE to see how the parameter influences the sound. When playing the microGranny by sending MIDI notes, the TUNED parameter selects whether the notes transpose the sound or play individual grains. See the MIDI chapter for more information.

LEGATO if turned on, the MIDI notes sent to the microGranny are transposing the pitch without resetting the start position and envelope, while more than one MIDI note is held. Note: LEGATO can be turned on only when TUNED is turned on.

REPEAT if turned on, the playback position jumps back to the START position when the playback reaches the END playback position. When turned off the playback ends when reaching the END position. If SHIFT SPEED is negative the start and end positions are switched.

SYNC when turned on the GRAIN SIZE and END parameters automatically synchronize to the MIDI clock.

RANDOM SHIFT the shifting of the GRAIN loop in the sample can be set to random, meaning it randomly decides whether the SHIFT speed goes forward or backward each time the GRAIN loop is played to the end.  

## Presets and banks

One preset consists of 6 sounds and all their parameters. To load different presets hold down the PAGE / PRESET button and press one of the 6 square black buttons to load the corresponding preset. The display for example shows PR.23, meaning you loaded preset number 3 (second numbers) from bank 2 (first number). To save a preset, hold down the FN button and press the RECORD button.

In one bank there are six presets. To change banks, hold down the PAGE / PRESET button and press UP or DOWN. There are 10 banks (0-9).

All of the presets are stored on the SD card in the form of simple .txt files, named P23.txt, for example. You can name and rearrange your presets on your computer.

## Recording

microGranny can record 8 bit samples with a sample rate of 22,050 Hz. It uses the on-board microphone or line input. When the line input is connected the microphone is disabled.  

Press the RECORD button to enter the record mode (the RGB LED turns RED). The dots on the display indicate the level of the incoming signal. Use the input volume knob to adjust the volume. Pressing the HOLD button will activate or deactivate the sound coming from the input to the output while in record mode.

After entering the record mode, the display asks you to select ("SLCT") a position where you want to record. Now press one of the six square black buttons. microGranny checks if there is a file in this slot and deletes it and prepares for recording. Then the display says ("REDY") and the RECORD LED starts blinking to indicate that you should hit the RECORD button to start recording. microGranny will turn off the display (to minimize noise) and will start recording (indicated only by the RECORD LED and the LED of the current slot). To stop recording, hit the RECORD button again. The recorded sound is now stored and assigned to the slot. You can exit the record mode by pressing the PAGE button.

For each square black button in each preset there is one file reserved for recording. Only the wave files with number, for example "2D.wavs", can be deleted and overwritten. The first character of the name of the sample refers to the bank, the second character refers to big button and preset (in preset 21 the reserved files for recording are 20-25 .wav, in P22 the reserved files are 26-2B .wav, in P23 the files are 2C-2H.wav, etc).

Note: recording automatically saves preset.  

Attention: do not turn off the microGranny while it is recording. It might result in corrupted files or a broken file system on the microSD card. If you are having problems of this kind, it is advised to format the microSD card again.

## MIDI channel

microGranny has MIDI input. It reads MIDI messages on the specified MIDI channel. To set the MIDI channel, hold down one of the big buttons while turning on the microGranny, to set the input channel to 1-6. By doing the same procedure while the FN button is pressed, you set the input channel to 7-12. The input channel is indicated on the display each time you turn on the microGranny, for example "CH 2" for MIDI input channel 2.

## MIDI notes

microGranny reads note messages and reacts to velocity. The first six notes of the lowest MIDI octave correspond to the 6 buttons on the microGranny.  

If the TUNED parameter is on, the last played sound gets spread and transposed on the keyboard in the range of three and a half octaves. The middle C note is the original pitch of the sample (C4 - note 60). The transposed mode is active from 3 octaves below this note (C1 - note 24) to 6 semitones above this note (F4 - note 65).

If the TUNED parameter is off, the range of 5 octaves (with C4 in the middle) represents the whole sample and pressing different keys sets starting position of the playback. When used with granular settings this feature can be used to play individual grains.

Tip: in case you happen to have some hanging MIDI notes, turning on and off the HOLD function will reset the MIDI note buffer.

## MIDI CCS

microGranny reacts to MIDI CC messages to set the parameters of the sound.
* CC   0 PRESET CHANGE
* CC   1 MODULATION WHEEL, sets GRAIN SIZE too
* CC  64 SUSTAIN
* CC 102 SAMPLE RATE
* CC 103 CRUSH
* CC 104 ATTACK
* CC 105 RELEASE
* CC 106 GRAIN SIZE
* CC 107 SHIFT SPEED
* CC 108 START
* CC 109 END
* CC 127 randomize

## MIDI side chain compression

This feature adds the ability to render attack again any time while the sound is playing, after receiving a specific MIDI note on the MIDI input. This results in a side chain compressor effect.

You can set the SIDE CHANNEL, SIDE NOTE and SIDE DECAY for this feature while you turn the microGranny on.

To set the SIDE CHANNEL hold down the UP button and one of the six square black buttons to set the channel to 1-6, and with the FN button held to 7-12.

To set the SIDE NOTE, hold the DOWN button and one of the six square black buttons to set the side note to 0-5 and with the FN button held to 60-65.

To set the SIDE DECAY, hold down both the UP and DOWN buttons and one of the six square black buttons to set different lengths of the decay. Setting the SIDE DECAY to the first button makes it the same value as the attack of the sound.

## MIDI out / thru and chaining

microGranny also has chain connectors to interface with other BASTL instruments. This allows you to easily add a sequencer / arpeggiator or drum machine. microGranny cannot merge MIDI signals coming from its MIDI input connector with MIDI signals coming from the left side connector. Always use only one of these.  

microGranny has a built-in MIDI thru function. However there is no onboard output MIDI connector. You can simply attach the MIDI BASTL instrument (set as output) to the right side connectors to add the MIDI thru connector.

## Preparing the SD card and your own samples

You can use your own sounds and you can use any microSD card you want. Before you use the card, format it with the official formatter to make it work faster, which can be found at www.sdcard.org/downloads.

You can use any microSD card reader that shows the card on your computer as an external drive. The samples for microGranny have to be wav files, mono, 16 or 8 bit and with a sample rate of 22,050 Hz. To convert your samples to this format, you can use the free software Audacity.

In Audacity, convert to mono, then change the project rate (bottom left corner) to 22,050 H and then go to File > Export. Choose Wave and use a name with only two letters, use A-Z (uppercase) and 0-9. Have a look at the factory SD card if you are not sure how to name the samples.  

Samples starting with a number (like 2B.wav) are reserved for recording and can be deleted and overwritten from within the microGranny.

Copy the files to the root directory on the SD card and everything should be ready to be played by the microGranny.
