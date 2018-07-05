# Moog Minitaur

## Installation

You can download and install a Minitaur editor, available from Moog's website.

## Power  

12 VDC center-positive power supply

## Jacks, switches and knobs

### Front panel

* MIDI: LED
* FINE TUNE: knob
* VCO 2 FREQ: knob
* FILTER CUTOFF: knob
* FILTER RES: knob
* FILTER EG AMOUNT: knob
* VCA VOLUME: knob
* OSCILLATORS 1: button
* OSCILLATORS 2: button
* MIX VCO 1 LVL: knob
* MIX VCO 2 LVL: knob
* ENVELOPES FILTER ATTACK: knob
* ENVELOPES FILTER DECAY / RELEASE: knob
* ENVELOPES FILTER SUSTAIN: knob
* ENVELOPES AMPLIFIER ATTACK: knob
* ENVELOPES AMPLIFIER DECAY / RELEASE: knob
* ENVELOPES AMPLIFIER SUSTAIN: knob
* MOD LFO RATE: knob
* MOD VCO LFO AMT: knob
* MOD VCO LFO AMT: knob
* RELEASE / POWER: button
* GLIDE RATE: knob
* GLIDE / POWER: knob

### Back panel

* HEADPHONES OUT: 1/8" stereo TRS headphone jack.
* AUDIO OUT: 1/4" TS output jack
* AUDIO IN: 1/4" TS output jack
* CONTROLLER INPUTS PITCH CV: jack
* CONTROLLER INPUTS FILTER CV: jack
* CONTROLLER INPUTS VOLUME CV: jack
* CONTROLLER INPUTS GATE: jack
* MIDI IN: MIDI DIN jack
* USB MIDI: USB-B jack
* 12V DC: center positive power jack

## Overview and features

OSCILLATORS: two Voltage Controlled Oscillators with selectable sawtooth (original Taurus) and Square waveshapes.

MIX: mixer for adjusting VCO levels independently.

FILTER: classic Moog 24 dB/Octave Low Pass Filter with adjustable Resonance.

ENVELOPES: twin Minimoog style ADSR Envelope Generators for modulating the Filter (VCF) and Amplifier (VCA). The Envelope Decay and Release segments are controlled by the DECAY knob, while the Release segment is enabled or disabled via the RELEASE switch.

MOD: MIDI-syncable Low Frequency Oscillator (LFO) with Rate control and an individual VCO and VCF AMOUNT controls.

HEADPHONE OUT: 1/8" stereo headphone output.

AUDIO OUT: 1/4" unbalanced output.

AUDIO IN: external audio input for processing audio through the Mixer and Filter section of the Minitaur.

CONTROL INPUTS: analog control inputs for Pitch, Filter, Volume and Gate. Use control voltage or a Moog EP2 expression pedal to connect and control the Minitaur with everything from Moogerfoogers to modular systems.

MIDI: DIN MIDI and USB MIDI offer complete control of the Minitaur's sound engine.

## Signal flow

The Minitaur's source signals are created by two Voltage-Controlled Oscillators (VCO) which are mixed with the External Audio Input. The Mixer Output is routed to the Filter, where the tone is sculpted according to the Filter parameters and the Filter ADSR Envelope. The signal is then passed to the Amplifier (VCA) stage, where the Volume ADSR envelope shapes it. Finally, the signal is routed to the Output section, where the final level is set by the Volume control knob.

For most users, MIDI will be the main source of control for the Minitaur. Each time the Minitaur receives a MIDI Note On command, it produces a Pitch CV and Gate signal in response. The Pitch CV signal sets the Pitch of the Oscillators, while the Gate signal triggers the Filter and Volume ADSR Envelopes.

The Minitaur can also be operated via CV and Gate trigger connections, for a more "old school" method of control. Both control methods (MIDI and CV/Gate) can be used at the same time, although some combinations of control signals may cause unpredictable results.

Note: DIN MIDI IN is not passed to USB MIDI OUT.

## Basic operation

The Minitaur responds to MIDI messages on both DIN and USB MIDI inputs. In addition, Minitaur's knobs and switches transmit MIDI Control Change (CC) commands via MIDI USB, allowing parameter adjustments to be captured by any MIDI-recording device. Minitaur has a LED MIDI indicator that indicates MIDI activity on either the DIN MIDI or USB MIDI connector. To further extend the Minitaur's capabilities, there are additional parameters that can be accessed via MIDI control.

## The components

### Oscillators

The oscillators are the main sound source of the Minitaur. They create electronic vibrations that can be tuned and amplified into sound that we can hear. The Minitaur's VCOs can produce a total musical range of six octaves.

Oscillator 1 (VCO 1) serves as a master oscillator to which oscillator 2 (VCO 2) is tuned. Two independent switches select the waveform for each oscillator (sawtooth or square). A FINE TUNE control adjusts the master tuning of both oscillators.

The frequencies of both oscillators are affected by a number of sources. The main source is a Note On command transmitted from an external MIDI controller or DAW. The Note On command is translated into a Control Voltage that allows the oscillators to be played in an equal-tempered scale. Other control sources include Minitaur's GLIDE circuit, VCO 2 FREQ, the PITCH CV INPUT, the FINE TUNE control, and the output of the MODULATION (LFO) circuit. The highest pitch produced by Minitaur's oscillators is C5 (523.25 Hz) or MIDI note value 72.

#### Panel control for the oscillator

OSCILLATOR 1 switch (CC 70): selects a sawtooth (LED OFF) or square wave (LED ON) for VCO 1.

OSCILLATOR 2 switch (CC 71): selects a sawtooth (LED OFF) or square wave (LED ON) for VCO 2.

VCO 2 FREQ (CC 17): sets the frequency offset of VCO 2 from VCO 1. The offset range is +/-1 octave. Center position tunes VCO 2 in unison with VCO 1. Note: if playing between notes 60 and 72, the pitch of VCO 2 is limited to note 72 (C4) regardless of this control setting.

FINE TUNE: adjusts the frequency of both VCOs by approximately +/-1 semitone. The FINE TUNE control does not transmit MIDI.

#### MIDI accessible control

VCO 2 BEAT (CC 18): selects the fine frequency offset for VCO 2. The adjustment range is +/- 50 cents. Default = 64.

NOTE SYNC (CC 81): when enabled, NOTE SYNC forces both oscillators to start at the same time, eliminating any phase differences at the start of each Note On command. This ensures energy is consistent at the start of each new note. Default = OFF.

#### External control

The PITCH CV jack on the back panel is a CV input for external control of the oscillator pitch. This input controls the frequencies of both oscillators. A 1 Volt change of this voltage will change the pitch by one octave. The jack accepts 0 to +5 Volts, or an expression pedal like the Moog EP-2.

Performance tips:

* For punchy bass lines, try using NOTE SYNC to keep the energy at the beginning of each note the same.
* A steady control voltage applied to the PITCH jack will offset the base pitch of both oscillators. You can use this feature to transpose the oscillators to any desired interval.
* To recreate the classic Taurus sound, choose the sawtooth wave for one or both oscillators.

### Glide

GLIDE (aka portamento) is a musical effect that makes smooth changes in pitch between notes. The Minitaur's GLIDE RATE is adjustable from instantaneous to extremely long.

#### Panel controls for glide

GLIDE switch (CC 65): enables/disables the GLIDE function, GLIDE is on when the LED is on.

GLIDE RATE (CC 5): sets the rate of GLIDE that occurs when the note controlling the Minitaur changes.

#### MIDI accesible control

GLIDE TYPE (CC 92): the Minitaur offers three GLIDE types: Linear Constant Rate (LCR), Linear Constant Time (LCT), or Exponential (EXP). When LCR is selected, the GLIDE RATE stays the same regardless of teh interval. When LCT is selected, the GLIDE TIME stays the same regardless of the interval. When EXP is selected, the GLIDE RATE follows an exponential curve that starts fast and then sows as it approaches the target note (like the Taurus). Default = LCR.

LEGATO GLIDE (CC 83): normally, GLIDE occurs with every new note. When LEGATO GLIDE is enabled, however, GLIDE is only applied when a new note is received while another note is still being held. Default = OFF.

### Mix (oscillator levels)

Each oscillator (VCO 1 and VCO 2) has a dedicated level knob that allows you to control the relative strength of each oscillator from 0 to 100%. NOTE: the VCOs begin to clip the filter at about 2 o'clock creating more agressive sounds.

#### Panel controls for the mixer

VCO 1 LVL (CC 15): sets the level of VCO 1.

VCO 2 LVL (CC 16): sets the level of VCO 2.

#### MIDI accessible control

EXTERNAL INPUT LEVEL (CC 27): adjusts the External Audio Input level. By default, the level is set for unity gain, but the level can be adjusted up to 200%. Default = 64.

### Filter

The FILTER is a classic Moog 24 dB/Octave Low-Pass Filter design with resonance. It has controls for CUTOFF frequency which determines the range of frequencies the filter will affect, as well as RESONANCE, which determines how much emphasis is applied to the harmonics near the Cutoff frequency.

The FILTER provides either fixed or dynamic timbre modifications. Dynamic changes are provided by the Filter Envelope Generator (EG), a Low Frequency Oscillator (LFO), or by an externally applied Control Voltage.

#### Panel controls for the filter

CUTOFF (CC 19): adjusts the CUTOFF frequency of the Low Pass Filter from 20 Hz to 20 kHz. As the knob is rotated clockwise, the cutoff frequency is increased, allowing more harmonics to pass through the filter, resulting in a brighter sound. Conversely, as the knob is rotated counterclockwise, the sounds get darker. Note: the Minitaur may not produce sound when this control is turned all way down.

RESONANCE (RES) (CC 21): sets the amount of signal sent from the FILTER output to be fed back into its input. This creates a peak in the frequency that can be increased all the way to self-oscillation.

EG AMOUNT (CC 22): determines how much the Filter Envelope Generator (EG) adds to or subtracts from the Filter Cutoff control setting. When the EG AMOUNT knob is set to positive (+), turn the FILTER CUTOFF knob left to hear the effect. When the EG AMOUNT knob is set to negative (-), turn the FILTER CUTOFF knob right to hear the effect. Note that if the Cutoff frequency is set very high, a positive EG Amount may have little or no noticeable effect, regardless of the setting. Similarly, if the Cutoff frequency is set low, a negative EG Amount may have little or no noticeable effect.

#### MIDI accesible control

FILTER KB TRACKING (CC 20): determines how the Filter Cutoff changes in response to MIDI note on values. Filter tracking is adjustable from 0 to 200%. Default = 32 (about 50%).

FILTER VELOCITY SENSITIVITY (CC 89): sets the amount of MIDI note velocity to the filter. Default = 64.

#### External control

The FILTER CV jack on the back panel is an input for external control of the Filter Cutoff parameter. A voltage applied to this jack is added to the setting of the Filter Cutoff control. A one Volt change in the Control Voltage will change the cutoff frequency of the filter by about one octave. The jack accepts 0 to +5 Volts, or an expression pedal like the Moog EP-2.

### Envelopes

ENVELOPE GENERATORS (EGs) add motion to a sound after a note is played. The Minitaur has two separate Minimoog style Envelope Generators that affect the brigthness and loudness of the Minitaur's sound by modulating the Filter Cutoff (VCF) and Volume (VCA).

The EGs are started by a Gate or MIDI note message. Once started, their shape in time is set by the ATTACK, DECAY/RELEASE, and SUSTAIN controls, as well as the Release switch and length of the note played.

#### Panel controls for the envelopes

FILTER ATTACK (CC 23): sets the time it takes for the Attack portion of the Filter EG to rise from zero to maximum. The Attack time ranges from 1 msec to 30 seconds.

FILTER DECAY/RELEASE (CC 24): sets the time for the Decay and Release portion of the Filter EG. When a note is held, and the Attack time end is reached, the Decay portion of the EG starts. During the Decay portion, the EG moves to the Sustain level. When a note is released, the EG moves back to zero at the rate set by this control. This time ranges from 1 msec to 30 seconds. The Release segment of the Envelope is determined by the state of the RELEASE switch (ON/OFF).

FILTER SUSTAIN (CC 25): sets the filter EG level after the Decay and before the Release portion. A note must be held longer than both the Attack and Decay time to reach the Sustain level. The level is adjustable from 0 to 100%.

AMPLIFIER ATTACK (CC 28): sets the time it takes for the Attack portion of the Amplifier EG to rise from zero to maximum. The Attack time ranges from 1 msec to 30 seconds.

AMPLIFIER DECAY/RELEASE (CC 29): sets the time for the Decay and Release portion of the Amplifier EG. When a note is held, and Attack time end is reached, the Decay portion of the EG starts. During the decay portion, the EG moves to the Sustain level. When a note is released, the EG moves back to zero at the rate set by this control. The time ranges from 1 msec to 30 seconds. The Release segment of the Envelope is determined by the state of the RELEASE switch (ON/OFF).

AMPLIFIER SUSTAIN (CC 30): sets the Amplifier EG level after the Decay and before the Release portion. A note must be held longer than both the Attack and Decay time to reach the Sustain level. The level is adjustable from 0 to 100%.

#### MIDI accessible control

OUTPUT (VCA) VELOCITY SENSITIVITY (CC 90): sets the amount of MIDI note velocity to the amplifier. Default = 64 (50%).

#### External CV control

The GATE jack on the back panel is a trigger input that accepts a +5V Gate signal. Applying a Gate signal causes both Envelopes (Amplifier and Filter) to trigger simultaneously. Note: when a Gate signal is applied, it overrides triggering via MIDI. You will still be able to control the Oscillator pitch and Modulation amounts from a MIDI controller, but the envelopes will not retrigger until the Gate trigger is removed.

### Release

The RELEASE switch enables or disables the Release segment of both Envelope Generators. When enabled, the Envelope Release time is the same as the Envelope Decay time, and the DECAY control adjusts the time for both segments. When disabled, the Release segment does not occur and the Envelope stops abruptly in response to a Note Off message (or when the Gate CV goes to zero).

#### Panel control for Release

RELEASE switch (CC 72): enables/disables the release function for both Envelope Generators. RELEASE is enabled when the switch LED is ON.

### Modulation (MOD)

MODULATION is an important part in the creation of musically-expressive sounds. The Minitaur's MODULATION section provides a LFO with adjustable RATE and AMOUNT controls for the oscillators (VCO) and the Filter (VCF). The Low Frequency Oscillator (LFO) is a signal used to move the pitch of VCOs and the Filter Cutoff up and down automatically. A LFO can be used to simulate vibrato, create wobbling filter sweeps, or make interesting syntheizer sounds.

#### Panel controls for modulation

LFO RATE (CC 3): sets the frequency of LFO Modulation. The range is from 0.01 Hz to 10.0 Hz.  

VCO LFO AMOUNT (CC 13): sets the maximum amount the LFO moves the VCOs pitch up and down, up to +/- 1 octave. Modulation affects both Oscillators. Amounts above MIDI note 72 are clipped. If using a MIDI controller, the Mod Wheel (CC 1) is used to fade the LFO Pitch Modulation in and out.

VCF LFO AMOUNT (CC 12): sets the maximum amount the LFO moves the Filter Cutoff up and down, up to +/- 5 octaves. Amounts above 20 kHz or below 20 Hz are clipped. If using a MIDI controller, the Mod Wheel (CC 1) is used to fade the LFO Filter Modulation in and out.

#### MIDI accessible control

LFO MIDI SYNC ON/OFF (CC 87): enables or disables the ability of the Minitaur's LFO to sync to MIDI Clock messages. Default = On.

LFO SYNC CLOCK DIVISION (CC 86): selects the LFO Clock division when the LFO Sync Source is set to MIDI Clock. LFO Division Settings are listed on page 24. The LFO RATE control can also act as a Clock Divider. Default = 1/4.

LFO KEY TRIGGER (CC 82): re-triggers the start of the LFO cycle when a Note On message or KB Gate Control Voltage is received. Default = OFF.

Note: when the Minitaur powers up, the settings on the VCO LFO AMOUNT and VCF LFO AMOUNT controls have direct effect on the VCO and VCF. This behavior continues until the Minitaur receives a MIDI Mod Wheel command, from which point the Mod Wheel takes master control of the LFO modulation amount set by the Amount controls.s

### Volume (VCA)

The Minitaur features a monophonic Audio Output and a Headphone Output; both outputs appear on the back panel. Both outputs are adjusted simultaneously by the VOLUME control.

#### Panel control for volume

Volume: adjusts the output of the Voltage Controlled Amplifier (VCA) and Headphone levels. Rotating the control fully clockwise produces the maximum output. Rotating the control fully counterclockwise silences the Minitaur. The VOLUME control does not transmit or receive MIDI. This is a post VCA control.

#### MIDI accessible control

OUTPUT LEVEL (CC 7): adjusts the Audio Output and Headphone volume levels.

VOLUME VELOCITY SENSITIVITY (CC 90): velocity scales the amplitude of the Amplifier envelope. Similar to traditional touch sensitivity. Default = 64 (50).

#### External control

The VOL CV jack on the back panel is an input for external control of the Output level. A voltage of 0 Volts silences the Minitaur and a voltage of 5 Volts correspond to the output level set by the VOLUME control knob. The jack accepts a positive Control Voltage from 0 to 5 Volts, or an expression pedal like the Moog EP-2.

### Input / output panel

The back panel provides all of the input and output connections. In addition to AUDIO INPUT/OUTPUT jacks, there are CV and GATE inputs, connections for MIDI, and the Power Connector. The Minitaur does not have a power switch.

12VDC (Power INPUT): a barrel connector that accepts a +12VDC, tip positive power input from the power adaptor, which accepts a 100-240 VAC, 50-60 Hz.

CONTROLLER INPUTS: The PITCH, FILTER and VOLUME CV jacks supply power and will accept an expression pedal such as the Moog EP-2, or a Control Voltage from 0 to +5 Volts. The GATE input accepts a +5 Volt trigger signal.

MIDI (DIN AND USB): connections for DIN MIDI input and USB MIDI IN-OUT.

AUDIO IN: The AUDIO IN jack allows an external audio source to be mixed with the Minitaur's VCOs, and then routed to the Filter for processing. Although the Minitaur has no provisions for adjusting the level of this input on the front panel, the level is adjustable up to 200% via MIDI CC 27.

AUDIO OUT: the AUDIO OUT jack provides an unbalanced line-level signal for connecting to an amplifier or mixer.

HEADPHONE OUTPUT: 1/8" minijack for stereo Headphone Output. 32 Ohm or higher recommended impedance.

Performance tips:

* You can use the Minitaur to process any audio signal simply by plugging into the AUDIO IN jack. To hear the external audio signal, you will need a MIDI Note On message. To hear the external audio signal without issuing a Midi Note On message, apply +5V to the GATE jack. This will leave the Gate open, and the Amplifier Envelope will remai at its Sustain level until the Gate closes.
* The Minitaur's audio input is not limited to processing monophonic signals - it can work well for processing polyphonic signals, too. For example, connect the Audio Output of a MIDI-equipped polyphonic keyboard to the Minitaur's AUDIO IN jack, and turn the MIX level of VCO 1 and VCO 2 all the way down on the Minitaur. Now you have a polyphonic source affected by the Minitaur's Filter and Envelope circuits - a great way to warm up a sterile digital signal!

## MIDI operations

MIDI CHANNEL: The Minitaur sends and receives on a single MIDI channel. By default, the Minitaur is set to MIDI channel 1, but it can be set to any MIDI channel (1-16). To change the MIDI channel on the Minitaur:
* Connect your MIDI controller or DAW to the Minitaur.
* Adjust the controller (or DAW) to transmit the desired MIDI channel.
* On the Minitaur, press and hold all four panel switches (VCO 1 Wave, VCO 2 Wve, GLIDE and RELEASE). The panel switch LEDs will blink, indicating that the Minitaur is waiting to set the new MIDI channel. The next MIDI message that the Minitaur receives (a Note On, CC, Pitch Bend, etc....) will set the new channel.
* Once in learn mode, press a key on the MIDI controller (or send MIDI data from the DW). The Minitaur will reset its MIDI channel to match the channel being sent.

Changes to the Minitaur's MIDI channel are written to memory and are remembered on power down.

MIDI NOTE RANGE: the Minitaur responds to MIDI note values 0-72; note values of 73 and higher are ignored.

PITCH BEND RESPONSE: by default, the PITCH BEND RESPONSE of the Minitaur is set to +/- 3 semitones. The Pitch Bend up and down values can be adjusted independently by issuing new values for MIDI CC 107 (Pitch Bend UP) and CC 108 (Pitch Bend DOWN). See the MIDI CC messages table for the range of values.

MODULATION WHEEL (MOD WHEEL) RESPONSE: MIDI Mod Wheel messages control the maximum amount of modulation effect set by the VCO LMO AMT and VCF LFO AMT controls (MIDI CC 1).

MIDI CONTROL CHANGE (CC) MESSAGES: the tables on the following pages list all the MIDI CC messages for the Minitaur. Messages shown with an (M) indicate parameters which are only accessible via MIDI. Bolded values indicate the appropiate range for 7-bit messages (MSB).

Notes:
* The Minitaur sends 7-bit MIDI CC messages for all parameters. It can receive either 7-bit or 14-bit values for the parameters controlled by knobs, but only 7-bit values for parameters controlled by switches.
* For all parameters, the MSB indicates the 'regular' CC number, and the LSB indiactes the high-resolution 'fine' control value. If you are only sending 7-bit MIDI CC messages to the Minitaur, use the MSB number by itself. Note that when MSB-only messages are issued, the value range is always 0-27.

## A note about control parameters

LOCAL CONTROL OFF (CC 122): this parameter allows the front panel controls to send MIDI, but disconnects the Minitaur sound engine from direct control by the panel. Per the MIDI spec, only values of '0' and '127' work (0 = OFF, 127 = ON). If you are connected to a DAW using USB MIDI patched through, you may need this to avoid feedback artifacts. After changing the state of LOCAL CONTROL on/off, the Minitaur remembers the last setting after power down.

ALL SOUNDS OFF / ALL NOTES OFF (CC 120 OR 123): both of these parameters are MIDI 'panic' functions that are used to silence hung MIDI notes. Controllers or DAWs may send one or the other command which is why the Minitaur will respond to either.

|Section|Control/Param         |Function          |CC              |Value|
|-------|----------------------|------------------|----------------|-----|
|MOD    |LFO RATE              |LFO freq          | 3 (MSB) 35(LSB)|0-127|
|MOD    |LFO VCO AMT           |Mod amt VCO       |13 (MSB) 45(LSB)|0-127|
|MOD    |LFO VCF AMT           |Mod amt VCF       |12 (MSB) 44(LSB)|0-127|
|MOD    |LFO MIDI SYNC (M)     |MIDI clock sync   |87              |0-63 (INT)|
|MOD    |LFO SYNC CLOCK DIV (M)|LFO sync clock div|86              |0-127|
|MOD    |LFO KEY TRIGGER (M)   |re-trigger LFO    |82              |0-127|

etc etc etc

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
