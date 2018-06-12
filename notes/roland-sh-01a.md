# maquinitas

## notes on roland sh-01a

to use midi through usb, install the driver available from the roland website.

midi implementation chart

|function                      |transmitted   |recognized |remarks      |
|------------------------------|--------------|-----------|-------------|
|basic channel default         |1-16          |1-16       |             |
|basic channel changed         |1-16          |1-16       |             |
|mode default                  |mode 3        |mode 3     |             |
|mode messages                 |mode 3        |mode 3     |             |
|mode altered                  |mode 3        |mode 3     |             |
|note number: true voice       |0-127         |0-127      |             |
|velocity: note on             |o             |o          |             |
|velocity: note off            |x             |x          |             |
|aftertouch                    |x             |x          |             |
|pitch bend                    |o             |o          |             |
|control change  1             |o             |o          |check details|
|control change  3             |o             |o          |check details|
|control change  5             |o             |o          |check details|
|control change 11             |x             |o          |check details|
|control change 12-31          |o             |o          |check details|
|control change 64,65          |x             |o          |check details|
|control change 71-87          |o             |o          |check details|
|program change                |0-63          |0-63       |             |
|system exclusive              |x             |x          |             |
|system common: song position  |x             |o          |             |
|system common: song select    |x             |x          |             |
|system common: tune request   |x             |x          |             |
|system real time: clock       |o             |o          |             |
|system real time: start       |o             |o          |             |
|system real time: continue    |x             |o          |             |
|system real time: stop        |o             |o          |             |
|aux msg: all sound off        |x             |o          |             |
|aux msg: reset all controllers|x             |o          |*1           |
|aux msg: local on/off         |x             |x          |             |
|aux msg: all notes off        |x             |o          |             |
|aux msg: omni mode off        |x             |o          |*1           |
|aux msg: omni mode on         |x             |o          |*1           |
|aux msg: mono mode on         |x             |o          |*1           |
|aux msg: poly mode on         |x             |o          |*1           |
|aux msg: active sensing       |x             |o          |             |
|aux msg: system reset         |x             |x          |             |

notes:
* 1: same process as all note off.

modes:
* 1: omni  on, poly  
* 2: omni off, poly  
* 3: omni  on, mono  
* 4: omni off, mono  

signs:
* o: yes
* x: no

control change list

|control change |explanation            |
|---------------|-----------------------|
| 1             |modulation             |
| 3             |lfo rate               |
| 5             |portamento time        |
|11             |expression pedal       |
|12             |lfo wave form          |
|13             |vco mod depth          |
|14             |vco range              |
|15             |vco pulse width        |
|16             |vco pwm source         |
|17             |vco mod sens           |
|18             |vco bend depth         |
|19             |vco pwm level          |
|20             |vco saw level          |
|21             |vco sub level          |
|22             |vco noise level        |
|23             |vco env depth          |
|24             |vcf env depth          |
|25             |vcf mod depth          |
|25             |vcf mod depth          |
|26             |vcf key follow         |
|27             |vcf bend depth         |
|28             |vca env sw             |
|29             |vca env mode           |
|30             |env sustain            |
|31             |portament mod          |
|64             |hold                   |
|65             |portamento             |
|71             |vcf resonance          |
|72             |env release            |
|73             |env attack             |
|74             |vcf cutoff             |
|75             |env decay              |
|76             |tune                   |
|77             |transpose sw           |
|78             |noise mode             |
|79             |lfo mode               |
|80             |assign mode            |
|81             |chord voice 2 sw       |
|82             |chord voice 3 sw       |
|83             |chord voice 4 sw       |
|85             |chord voice 2 key shift|
|86             |chord voice 3 key shift|
|87             |chord voice 4 key shift|
