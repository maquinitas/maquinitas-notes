# maquinitas

## notes on cyclone analogic tt-78 beat bot

this device has midi input and output.

channel 3 is the default midi in and midi out channel.

the beat bot responds to midi note on messages for each of its drum instruments. it responds to them in all four of its modes.

midi notes with a velocity value above 112 are considered to be accented drum strikes.

it responds to continous controller CC messages for adjusting the tone values of each of its instruments.

beat bot will automatically sync its sequencer to a midi clock received from an external midi source. it will respond to external start commands, stop commands, continue messages, and clock information.

to set the midi in channel, press [FUNCTION]+[15], the key labeled MIDI IN. the currently selected midi channel will have a brigthtly lit led while the others will be dim. select the new midi channel by pressing a numbered key. press FUNC to exit. the operation is similar for MIDI OUT, accessible via [FUNCTION]+[16].

midi implementation chart

|function                   |transmitted |recognized      |remarks            |
|---------------------------|------------|----------------|-------------------|
|basic channel              |1-16        |1-16            |factory is 3       |
|mode                       |4           |4               |                   |
|mode                       |            |omni off, mono  |                   |
|note number 36             |o           |o               |bass drum (BD)     |
|note number 38             |o           |o               |snare drum (SD)    |
|note number 64             |o           |o               |low conga (LC)     |
|note number 63             |o           |o               |high conga (HC)    |
|note number 61             |o           |o               |low bongo (LB)     |
|note number 60             |o           |o               |high bongo (HB)    |
|note number 42             |o           |o               |hi-hat (HH)        |
|note number 51             |o           |o               |cymbal (CY)        |
|note number 54             |o           |o               |tambourine (TB)    |
|note number 56             |o           |o               |cowbell (CB)       |
|note number 75             |o           |o               |clave (CL)         |
|note number 70             |o           |o               |maracas (MA)       |
|note number 73             |o           |o               |guiro (GU) short   |
|note number 74             |o           |o               |guiro (GU) long    |
|velocity note on           |V=64 normal,|V= 0 off,       |                   |
|                           |127 accent  |1-111 normal    |                   |
|                           |127 accent  |112-127 accent  |                   |
|velocity note off          |V=0         |any             |                   |
|aftertouch buttons         |x           |x               |                   |
|aftertouch channel         |x           |x               |                   |
|pitch bend                 |x           |x               |                   |
|control change 16          |x           |o (0,1,2,4,8,16)|auto-fill interval |
|control change 17          |x           |o               |flam time          |
|control change 18          |x           |o               |shuffle amount     |
|control change 20          |o           |o               |BD tone            |
|control change 22          |x           |o (0,31)        |BD nuance shape    |
|control change 23          |x           |o               |BD nuance amount   |
|control change 24          |x           |o               |BD gate/mute       |
|control change 28          |o           |o               |SD tone            |
|control change 30          |x           |o (0,31)        |SD nuance shape    |
|control change 31          |x           |o               |SD nuance amount   |
|control change 32          |x           |o               |SD gate/mute       |
|control change 36          |o           |o               |LC tone            |
|control change 37          |o           |o               |LB tone            |
|control change 38          |x           |o (0,31)        |LC/LB nuance shape |
|control change 39          |x           |o               |LC/LB nuance amount|
|control change 40          |x           |o               |LC/LB gate/mute    |
|control change 44          |o           |o               |HC tone            |
|control change 45          |o           |o               |HB tone            |
|control change 46          |x           |o (0,31)        |HC/HB nuance shape |
|control change 47          |x           |o               |HC/HB nuance amount|
|control change 48          |x           |o               |HC/HB gate/mute    |
|control change 52          |o           |o               |CL tone            |
|control change 53          |o           |o               |CB tone            |
|control change 54          |x           |o (0,31)        |CC/CB nuance shape |
|control change 55          |x           |o               |CC/CB nuance amount|
|control change 56          |x           |o               |CC/CB gate/mute    |
|control change 60          |o           |o               |CY tone            |
|control change 62          |x           |o (0,31)        |CY nuance shape    |
|control change 63          |x           |o               |CY nuance amount   |
|control change 64          |x           |o               |CY gate/mute       |
|control change 68          |o           |o               |HH tone            |
|control change 70          |x           |o (0,31)        |HH nuance shape    |
|control change 71          |x           |o               |HH nuance amount   |
|control change 72          |x           |o               |HH gate/mute       |
|control change 76          |o           |o               |MA tone            |
|control change 78          |x           |o (0,31)        |MA nuance shape    |
|control change 79          |x           |o               |MA nuance amount   |
|control change 80          |x           |o               |MA gate/mute       |
|control change 84          |o           |o               |TB tone            |
|control change 85          |o           |o               |GU tone            |
|control change 86          |x           |o (0,31)        |TB/GU nuance shape |
|control change 87          |x           |o               |TB/GU nuance amount|
|control change 88          |x           |o               |TB/GU gate/mute    |
|program change             |x           |x               |                   |
|system exclusive           |o           |o               |backup, updates    |
|system common song position|x           |x               |                   |
|system common song select  |x           |x               |                   |
|system common tune         |x           |x               |                   |
|system real time clock     |o           |o               |                   |
|system real time commands  |start/stop  |start/stop/cont.|                   |
|aux messages               |x           |x               |                   |
