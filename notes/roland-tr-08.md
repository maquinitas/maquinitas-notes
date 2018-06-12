# maquinitas

## notes on roland tr-08

to use midi through usb, install the driver available from the roland website.

to factory reset, turn off. hold down the button 2 and turn on. tap will blink, you can cancel factory reset by turning off. if you want to continue, press the tap button to execute the factory reset. when all buttons blink, the display says done, and you can turn off and on again.

menu mode:

* press the menu button
* use the value knob to select an item
* press the tap button.
* each time you press the tap button, you can switch between selecting an item and editing its value.

|item (parameter)        |value       |explanation                            |
|------------------------|------------|---------------------------------------|
|comp (comp)             |0 - 100     |level of compression level to bd and sd|
|gain (gain)             |0 to 200    |gain, buttons 2-12 select drum sound   |
|tune (tune)             |-128 - 127  |pitch of bd, rs,cp,cb,oh,ch            |
|decy (decay)            |-128 - 127  |decay length sd,lt,mt,ht,rs,cp,cb,ch   |
|pan (pan)               |l64..c0..r63|pan of each instrument                 |
|bd (bd type)            |nrm, l.dcy  |type of bd, normal or long decay       |
|h. lnk (hihat link)     |off, on     |if on, ch settings follow oh settings  |
|ch (midi channel)       |1 - 16,off  |selects midi transmit/receve channel   |
|sync (midi clock source)|auto,int    |auto follows midi clock if being input |
|a. off (auto off)       |off,30min   |auto off does not work with usb power  |
|demo (led demo)         |off,1,3,10  |time until unit enters led demo mode   |

midi implementation chart

|function                      |transmitted|recognized|remarks                 |
|------------------------------|-----------|----------|------------------------|
|basic channel default         |1          |1         |memorized               |
|basic channel changed         |1-16, off  |1-16, off |                        |
|mode default                  |mode 3     |mode 3    |*1                      |
|mode messages                 |x          |x         |*1                      |
|mode altered                  |********** |**********|                        |
|note number:                  |*1         |*2        |                        |
|note number: true voice       |********** |0-127     |                        |
|velocity: note on             |o          |o         |                        |
|velocity: note off            |o          |o         |                        |
|aftertouch key's              |x          |x         |                        |
|aftertouch channel's          |x          |x         |                        |
|pitch bend                    |x          |x         |                        |
|control change 20-29          |o          |o         |check details           |
|control change 46-63          |o          |o         |check details           |
|control change 71             |o          |o         |check details           |
|control change 80-88          |o          |o         |check details           |
|program change                |x          |x         |                        |
|program change: true number   |********** |**********|                        |
|system exclusive              |x          |x         |                        |
|system common: song position  |o          |o         |                        |
|system common: song select    |x          |x         |                        |
|system common: tune request   |x          |x         |                        |
|system real time: clock       |o          |o         |                        |
|system real time: start       |o          |o         |                        |
|system real time: continue    |o          |o         |                        |
|system real time: stop        |o          |o         |                        |
|aux msg: all sound off        |o          |o         |transmitted:midi offline|
|aux msg: reset all controllers|o          |o         |transmitted:midi offline|
|aux msg: local on/off         |x          |x         |                        |
|aux msg: all notes off        |o          |o         |transmitted:midi offline|
|aux msg: omni mode off        |x          |o         |*2                      |
|aux msg: omni mode on         |x          |o         |*2                      |
|aux msg: mono mode on         |x          |o         |*2                      |
|aux msg: poly mode on         |x          |o         |*2                      |
|aux msg: active sensing       |o          |o         |                        |
|aux msg: system reset         |x          |x         |                        |

notes:
* 2: the same processing will be carried out as when all notes off is received.

modes:
* 1: omni  on, poly  
* 2: omni off, poly  
* 3: omni  on, mono  
* 4: omni off, mono  

signs:
* o: yes
* x: no

* 1:

|instrument   |note number|
|-------------|-----------|
|bass drum    |36         |
|rim shot     |37         |
|snare drum   |38         |
|hand clap    |39         |
|closed hi-hat|42         |
|low tom      |43         |
|open hi-hat  |46         |
|mid tom      |47         |
|cymbal       |49         |
|high tom     |50         |
|cow bell     |56         |
|high conga   |62         |
|mid conga    |63         |
|low conga    |64         |
|maracas      |70         |
|claves       |75         |

* 2:

|instrument   |note number|
|-------------|-----------|
|bass drum    |35, 36     |
|rim shot     |37         |
|snare drum   |38, 40     |
|hand clap    |39         |
|closed hi-hat|42, 44     |
|low tom      |41, 43     |
|open hi-hat  |46         |
|mid tom      |45, 47     |
|cymbal       |49         |
|high tom     |48, 50     |
|cow bell     |51, 56     |
|high conga   |62         |
|mid conga    |63         |
|low conga    |64         |
|maracas      |70         |
|claves       |75         |

control change list

|control change 20-29          |o          |o         |check details           |
|control change 46-63          |o          |o         |check details           |
|control change 71             |o          |o         |check details           |
|control change 80-88          |o          |o         |check details           |

|control change |explanation|
|---------------|-----------|
|20             |bd tune    |
|21             |bd tone    |
|22             |bd comp    |
|23             |bd decay   |
|24             |bd level   |
|25             |sd tone    |
|26             |sd snappy  |
|27             |sd comp    |
|28             |sd decay   |
|29             |sd level   |
|46             |lt tune    |
|47             |lt decay   |
|48             |lt level   |
|49             |mt tune    |
|50             |mt decay   |
|51             |mt level   |
|52             |ht tune    |
|53             |ht decay   |
|54             |ht level   |
|55             |rs tune    |
|56             |rs decay   |
|57             |rs level   |
|58             |cp tune    |
|59             |cp decay   |
|60             |cp level   |
|61             |ch tune    |
|62             |ch decay   |
|63             |ch level   |
|71             |accent     |
|80             |oh tune    |
|81             |oh decay   |
|82             |oh level   |
|83             |cy tone    |
|84             |cy decay   |
|85             |cy level   |
|86             |cb tune    |
|87             |cb decay   |
|88             |cb level   |
