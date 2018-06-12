# maquinitas

## notes on critter and guitari bolsa bass

## physical layout

the jacks on the back are, from left to right:

* midi out
* midi in

the knobs on the upper-left corner of the front panel are, from left to right:

* knob 1: these knob controls parameters in the synthesizer's six modes.
* knob 2: these knob controls parameters in the synthesizer's six modes.
* tune knob: it can tune over a 1 octave range. when turned all the way to the left, the bottom key 'c' is a c2 (65.402 hz). Turning the knob all the way to the right raises the bottom key to c3 (130.804 Hz). the midi output is not affected by this knob.
* volume: it controls overall output of the synthesizer. it is hardwired to the output jack, so it does not affect the sequencing. (the other three knobs can be recorded).

on the upper-right side of the front panel, there is the power switch, the power supply jack (9 vdc center-positive), and line out (mono).

the sixteen wooden buttons on the bottom of the left panel are a midi keyboard, starting in c and ending in d#. they can also be used to select the midi channel of the device. the keys are not pressure sensitive, but they are aware of how long they are pressed.

the two wooden buttons on the bottom right, each one with a led over it, are the sequence button and the mode button.

## modes

|mode        |led light |
|------------|----------|
|circle ramp |red       |
|saw ramp    |yellow    |
|analog style|green     |
|sweep filter|light blue|
|fm pad      |blue      |
|bass delay  |magenta   |


circle ramp: downward ramping pure sine tone.  
* knob 1: ramp speed from very fast (<10 milliseconds) to very slow (1.5 seconds).
* knob 2: starting point of the downward ramp. all the way to the right is no ramp, all the way to the left is 2 octaves above.

saw ramp: similar to circle ramp, but using sawtooth tone. the tone in this mode is actually a summation of a sine wave and a sawtooth wave. the added sine wave bulks up the tone for a 'fatter' sound.  
* knob 1: ramp speed from very fast (<10 milliseconds) to very slow (1.5 seconds).
* knob 2: starting point of the downward ramp. all the way to the right is no ramp, all the way to the left is 2 octaves above.

analog style: classic resonant low-pass filter sound. a sawtooth wave is fed into the filter. the cutoff frequency is keyed to the note being played, so with the resonance turned up it's possible to emphasize specific harmonics in each note played.  
* knob 1: cutoff frequency, relative to the note being played.  
* knob 2: resonance.  

sweep filter: similar analog low-pass filter sound, but with a downward sweeping filter envelope.  
* knob 1: envelope time, from 10 milliseconds to 4 seconds.  
* knob 2: resonance.  

fm pad: dual oscillator fm synthesizer. two frequency modulated oscillators are added together. the harmonicty of each oscillator is controlled from a low frequency oscillator (lfo). the frequency of the second fm oscillator is offset to provide further phasing in the harmonics of the note played.  
* knob 1: lfo rate and oscillator frequency offset. turning this knob up increases the rate of the phasing effect. turn it all way down to stop the oscillation.  
* knob 2: index of modulation. turn this knob up to add more high frequency harmonics into the sound.  

bass delay: tuned delay line. a quick impulse is fed through a delay line with controllabe feedback and delay tine. the delay time is relative to the note being played which makes a string like sound.  
* knob 1: delay time. turn this knonb all the way down to set the delay time equal to the period of the note being played.   
* knob 2: feedback. turn this all the way up to sustain the note indefinitely.  

## midi info

the bolsa bass sends and receives midi note, midi clock, and midi start/stop commands. it can bes used as a stand alone controller, sound module, or as a sequencer. looking at the synthesizer from the top, midi out is the jack on the left, midi in is the jack on the right (the innermost jack).

### midi channel select

the bolsa bass sends and receives midi notes on channel 1 by default. to change send and receive channel (1-16), hold down the corresponding key during power up. the lowest note on the keyboard is channel 1, the highest note is channel 15. the bolsa bass will return to the default behavior of receiving channel 1 if turned off and no other key is held down during power up.

### note commands

the bolsa bass responds to all nnotes on the selected channel, so using an external keyboard allows for a much larger note range than the buil-in keyboard. any note received on the selected channel is also passed to the midi output.

the keyboard on the bolsa bass starts at midi note 36 (c2). any notes pressed on the keyboard are sent out as midi on the selected channel.

### clock

many synthesizers, drum machines, and sequenceres use midi clock to synchronize events. midi clock messages occur at 24 pulses or ticks per quarter note. the bolsa bass receives these midi clock messages. if a midi innput is connected, and there is midi clock present, the bolsa bass will latch onto that clock and disable its internal clock. the mode led will flash briefly at each quarter nonte if a midi clock innput is present. any midi clock received is passed directly thru to the midi output for syncing other devices.

### start/stop commands

the sequencer also responds to midi start and stop commands so it can be controlled externally. for example, if a drum machine is connected to the midi innput, starting the drum sequencer will also start the bolsa bass sequencer.

when the sequencer on the bolsa bass is started or stopped (either by pressing the button on the bolsa bass, or externally from a midi device), a midi start or stop command is sent out so that other downstream devices may be synchronized.  
