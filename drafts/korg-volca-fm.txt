# maquinitas

## notes on korg volca fm

this digital synthesizer uses a 3-voice, 6-operator fm (frequency modulation) sound engine.

in addition to the basic fm sound parameters, there are also a number of volca fm-specific parameters that provide further sound-editing capabilities.

sound files (sys-ex/syx) created on the yamaha dx-7 can be converted and loaded into the volca fm. sounds created on the volca fm can be exported and shared with another volca fm.

in addition, the volca fm also includes a built-in step sequencer, motion sequencer, and an arpeggiator -plus various voice modes- that can all add movement, depth, and expression to your volca fm sounds.

fm (frequency modulation) is based on synthesis elements known as operators. the volca fm sound engine uses six operators. operators can function as either modulators or carriers; modulating operators apply modulation to audio-source carrier operators interact is called an algorithm; the volca fm provides 32 distinct fm algorithms.

in the edit mode, the parameters required for the fm sound source, such as the lfo waveform and speed as well as the eg level and rate, can be set for each operator.

* transpose slider: this slider raises or lowers the pitch in units of octaves or semitones.

* velocity slider: in play mode, this slider controls the global velocity. in edit mode, this slider functions as the value slider for editing the fm synthesis parameters.  

* octave < >, operator +, - buttons: in play mode, these buttons change the octave range of the keyboard. in edit mode, these buttons select the operator to edit. by selecting "a" (all), you can edit parameters that apply to all operators.  

* save/export button: when not in edit mode, this button saves the fm sound engine parameters. press the save/export button, and then use the program knob to select the save location for the program. press the save/export button again to begin saving. to cancel the save operation, press the edit button before pressing the save/export button.

* exporting: you can connect the volca fm's sync out jack to the sync in jack of another volca fm unit, and export (transmit) fm sound programs and sequences to the other volca fm unit.  
in edit mode, press the save/export button so that the button blinks, and then use the program knob to select the item to be exported. after selecting the item to be exported, press the save/export button again to export it. the save/export button lights up while the export operation is being performed. the save/export button blinks again when the operation is finished.  
items to be exported: crnt pgn (currently selected program), all pgm (all 32 programs), crnt seq (current sequence), all seq (all 16 sequences), clone (all previously listed items).

edit button: use this button to toggle between the edit and play modes. edit mode is the mode for specifying settings for fm synthesis parameters and exporting.

### specifying global parameter settings

setting the midi channel:
* while holding down the memory button, turn the volca fm on.
* keyboard buttons 1 to 16 correspond to the midi channels 1 to 16. press the button that corresponds to the desired channel, and the led below the keyboard button will light up.

other parameters:
* while holding down func button, turn on the volca fm.
* use the keyboard buttons 1-8 to set your preferences for any or all of the global parameters.
* when you have finished, press the rec button. your settings will be saved, and the volca fm will restart. to cancel without making changes, press the play button.



with led lit:

|button|parameter              |status              |display indication|
|------|-----------------------|--------------------|------------------|
|1     |auto power-off function|*enabled            |autop on          |
|2     |battery type selection |nickel-metal hybride|batt nnh          |
|3     |sync out polarity      |fall                |syncot lo         |
|4     |sync in polarity       |fall                |syncin lo         |
|5     |tempo range settings   |full (10-600)       |tempo ful         |
|6     |midi clock src         |*auto               |mdclk aut         |
|7     |midi rx shortmessage   |*on                 |mdshrt on         |
|8     |sync input/output unit |once a step         |syncstp 1         |

with led unlit:

|button|parameter              |status             |display indication|
|------|-----------------------|-------------------|------------------|
|1     |auto power-off function|disabled           |autop of          |
|2     |battery type selection |*alkaline          |batt al           |
|3     |sync out polarity      |*rise              |syncot hi         |
|4     |sync in polarity       |*rise              |syncin hi         |
|5     |tempo range settings   |*narrow (56-240)   |tempo nar         |
|6     |midi clock src         |internal           |mdclk int         |
|7     |midi rx shortmessage   |off                |mdshrt of         |
|8     |sync input/output unit |*once every 2 steps|syncstp 2         |

factory default settings are marked with an asterisk *

the volca fm can be controlled via midi, simply connect the midi output of an external midi device to the midi in jack of the volca fm. the midi messages that can be received by the volca fm are listed in its midi implementation chart.

midi implementation chart

|function                   |transmitted   |recognized    |remarks           |
|---------------------------|--------------|--------------|------------------|
|basic channel default      |**************|1-16          |memorized         |
|basic channel changed      |**************|1-16          |                  |
|mode memorized             |x             |3             |                  |
|mode messages              |x             |x             |                  |
|mode altered               |**************|              |                  |
|note number                |**************|0-127         |                  |
|true voice                 |**************|0-127         |                  |
|velocity note on           |x             |x 9n, v=1-127 |                  |
|velocity note off          |x             |              |                  |
|aftertouch poly  (key)     |x             |x             |                  |
|aftertouch mono (channel)  |x             |x             |                  |
|pitch bend                 |x             |o             |*1                |
|control change 40          |x             |o             |transpose       *1|
|control change 41          |x             |o             |velocity        *1|
|control change 42          |x             |o             |modulator attack*1|
|control change 43          |x             |o             |modulator decay *1|
|control change 44          |x             |o             |carrier attack  *1|
|control change 45          |x             |o             |carrier decay   *1|
|control change 46          |x             |o             |lfo rate        *1|
|control change 47          |x             |o             |lfo pitch depth *1|
|control change 48          |x             |o             |algorithm       *1|
|control change 49          |x             |o             |arp type        *1|
|control change 50          |x             |o             |arp div         *1|
|program change             |x             |x             |                  |
|variable range             |**************|**************|                  |
|system exclusive           |x             |o             |*3                |
|system common song position|x             |o             |*2                |
|system common song select  |x             |x             |                  |
|system common tune         |x             |x             |                  |
|system real time clock     |x             |o             |*2                |
|system real time command   |x             |o             |*2                |
|aux messages local on/off  |x             |x             |                  |
|aux messages all notes off |x             |0 123-127     |*1                |
|aux messages active sense  |x             |0             |                  |
|aux messages reset         |x             |x             |                  |

notes:
* 1: received when global parameter midi rx shortmessage is set to on.
* 2: not received when global parameter midi clock src is set to internal; received when set to auto.
* 3: received only yamaha dx7 bulk data.

modes:
* mode 1: omni on, poly
* mode 2: omni on, mono
* mode 3: omni off, poly
* mode 4: omni off, mono

signs:
* o: yes
* x: no
