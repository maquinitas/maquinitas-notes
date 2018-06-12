# maquinitas

## notes on moog minitaur

* 12 vdc power adaptor
* midi input
* usb midi in

the minitaur is set to receive messages on midi channnel 1.

it is a bass synthesizer, so it operates exclusively in the lower note range (midi nnotes 0-72). this means that the minitaur will respond to your playing from 'c4' (an octave above middle c) downward.

a warm up period of about 15 minutes is recommended for the minitaur to reach concert pitch.

the minitaur is a monophonic analog bass synthesizer with a 100% analog audio path. it is based on the legendary taurus 1 and taurus 3 synthesizers. the minitaur features 2 ultra-stable voltage controlled oscillators, a genuine moog low pass filter, 2 envelope generators and a modulation circuit. the minitaur has a classic one knob per function design in a rugged performance package that is small enough to take with you anywhere.

### front panel

* oscillators: two voltage controlled oscillators with selectable sawtooth(original taurus) and square waveshapes.
* mix: mixer for adjusting vco levels independently.
* filter: classic moog 24db/octave low pass filter with adjustable resonance.
* envelopes: twin minimoog style adsr envelope generators for modulating the filter (vcf) and amplifier (vca). the envelope decay and release segments are controlled by the decay konb, while the release segment is enabled or disabled via the release switch.
* mod: midi-syncable low frequency oscillator (lfo) with rate control and individual vco and vcf amount controls.

### back panel

* headphone out: 1/8" headphone output.
* audio out: 1/4" unbalanced output.
* audio in: external audio input for processing audio through the mixer and filter section of the minitaur.
* control inputs: analog control inputs for pitch, filter, volume and gate. Use control voltage or a moog ep2 expression pedal to connect and control the minitaur with everything from moogerfoogers to modular systems.
* midi: din midi and usb midi offer complete control of the minitaur's sound engine.

### signal flow

the minitaur's source signals are created by two voltage-controlled oscillators (vco) which are mixed with the external audio input. the mixer output is routed to the filter, where the tone is sculpted according to the filter parameters and the filter adsr envelope. the signal is then passed to the amplifier (vca) stage, where the volume adsr envelope shapes it. finally, the signal is routed to the output section, where the final level is set by the volume control knob.

for most users, midi will be the main source of control for the minitaur. each time the minitaur receives a midi "note on" command, it produces a pitch cv and gate signal in response. the pitch cv signal sets the pitch of the oscillators, while the gate signal triggers the filter and volume adsr envelopes.

the minitaur can also be operated via cv and gate trigger connections, for a more 'old school' method of control. both control methods (midi and cv/gate) can be used at the same time, although some combinations of control signals may cause unpredictable results.

note: din midi inn is not passed to usb midi out.

### basic operation

the minitaur responds to midi messages on both din and usb midi inputs. in addition, minitaur's knobs and switches transmit midi control change (cc) commands via midi usb, allowing parameter adjustments to be captured by any midi-recordign device. minitaur has an led midi indicator that indicates midi activity on either the din midi or usb midi connector. to further extend the minitaur's capabilities, there are additional parameters that can be accessed via midi control. a complete list of all midi cc commands can be found on page 22-23.

### the components

TODO: this is page 6, to be continued...
