# maquinitas

## notes on cyclone analogic tt-303 bass bot mkii

this device has midi input and output.

set it to midi mode with the mode knob.

the bass bot responds to midi note on, assuming the pitch is within the bass bot's range.

midi notes with a velocity value above 112 are considered to be accented notes.

midi notes that overlap (a second note begins before the first note ends) are considered to be tied together, and the result will be similar to a note that has the slide modifier applied.

midi notes can also be used to activate patterns.

the bass bot will automatically sync its sequencer to a midi clock from an external midi source. it will respond to external start commands, stop commands, continue messages, and clock information.

only midi channels 1-12 are supported. channel 1 is the default midi in and midi out channel.

to set the midi in channel, press [FUNCTION]+[7], the key labeled MIDI IN. the currently selected midi channel will have a brigthly lit led while the others will be dim. select the new midi channel by pressing a numbered key. press FUNC to exit. the operation is similar for MIDI OUT, accesible via [FUNCTION]+[8].
