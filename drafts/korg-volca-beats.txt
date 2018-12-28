# maquinitas

## notes on korg volca beats

to set the midi channel, hold down the memory button and turn the volca beats on. step buttons 1 to 16 correspond to the midi channels 1 to 16. press the button that corresponds to the desired channel, the led below the step button will light up.

for setting other parameters, hold down the func button, turn on the volca beats. use the step buttons 1-8 to set your preferences for any or all of the global parameters. when finished, press the rec button. your settings will be saved and the volca beats will restart. to cancel without making changes, press the play button.

with led lit:

|button|parameter              |status              |display indication|
|------|-----------------------|--------------------|------------------|
|1     |auto power-off function|*enabled            |ap.on             |
|2     |battery type selection |nickel-metal hybride|bt.nh             |
|3     |sync out polarity      |fall                |so.lo             |
|4     |sync in polarity       |fall                |si.lo             |
|5     |tempo range settings   |full (10-600)       |tp.fl             |
|6     |midi clock src         |*auto               |cl.at             |
|7     |midi rx shortmessage   |*on                 |st.on             |

with led unlit:

|button|parameter              |status             |display indication|
|------|-----------------------|-------------------|------------------|
|1     |auto power-off function|disabled           |ap.of             |
|2     |battery type selection |*alkaline          |btal              |
|3     |sync out polarity      |*rise              |so.hi             |
|4     |sync in polarity       |*rise              |si.hi             |
|5     |tempo range settings   |*narrow (56-240)   |tp.nr             |
|6     |midi clock src         |internal           |cl.in             |
|7     |midi rx shortmessage   |off                |st.of             |

factory default settings are marked with an asterisk *

the volca beats can be controlled via midi, simply connect the midi output of an external midi device to the midi in jack of the volca kick. the midi messages that can be received by the volca beats are listed in its midi implementation chart.

midi implementation chart

|function                   |transmitted   |recognized    |remarks            |
|---------------------------|--------------|--------------|-------------------|
|basic channel              |**************|1-16          |memorized          |
|default changed            |**************|1-16          |                   |
|mode memorized             |x             |3             |                   |
|mode messages              |x             |x             |                   |
|mode altered               |**************|              |                   |
|note number                |**************|0-127         |*1                 |
|true voice                 |**************|36-75         |*1, *2             |
|velocity note on           |x             |x 9n, v=1-127 |                   |
|velocity note off          |x             |x             |                   |
|aftertouch poly (key)      |x             |x             |                   |
|aftertouch mono (channel)  |x             |x             |                   |
|pitch bend                 |x             |x             |                   |
|control change 40          |x             |o             |level kick       *1|
|control change 41          |x             |o             |level snare      *1|
|control change 42          |x             |o             |level lo tom     *1|
|control change 43          |x             |o             |level hi tom     *1|
|control change 44          |x             |o             |level cl hat     *1|
|control change 45          |x             |o             |level op hat     *1|
|control change 46          |x             |o             |level clap       *1|
|control change 47          |x             |o             |level claves     *1|
|control change 48          |x             |o             |level agogo      *1|
|control change 49          |x             |o             |level crash      *1|
|control change 50          |x             |o             |pcm speed clap   *1|
|control change 51          |x             |o             |pcm speed claves *1|
|control change 52          |x             |o             |pcm speed agogo  *1|
|control change 53          |x             |o             |pcm speed crash  *1|
|control change 54          |x             |o             |stutter time     *1|
|control change 55          |x             |o             |stutter depth    *1|
|control change 56          |x             |o             |tom decay        *1|
|control change 57          |x             |o             |closed hat decay *1|
|control change 58          |x             |o             |open hat decay   *1|
|control change 59          |x             |o             |hat grain        *1|
|program change             |x             |x             |                  |
|variable range             |**************|**************|                  |
|system exclusive           |x             |x             |                  |
|system common song position|x             |o             |*3                |
|system common song select  |x             |x             |                  |
|system common tune         |x             |x             |                  |
|system real time clock     |x             |o             |*3                |
|system real time command   |x             |o             |*3                |
|aux messages local on/off  |x             |x             |                  |
|aux messages all notes off |x             |x             |                  |
|aux messages active sense  |x             |0             |                  |
|aux messages reset         |x             |x             |                  |

notes:
* 1: received when global parameter midi rx shortmessage is set to on.
* 2: note numbers and corresponding parts 36: kick, 38: snare, 43: lo tom, 50: hi tom, 42: cl hat, 46: op hat, 39: clap
* 3: not received when global parameter midi clock src is set to internal; received when set to auto.

modes:
* mode 1: omni on, poly
* mode 2: omni off, poly
* mode 3: omni on, mono
* mode 4: omni off, mono

signs:
* o: yes
* x: no
