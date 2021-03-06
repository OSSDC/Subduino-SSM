# Subduino-SSM
Subaru Select Monitor to Canbus adapter

#Credits
This application carries the GNU General Public License and uses Open Source components. You can find the source code of their open source projects. I acknowledge and are grateful to these developers for their contributions to open source.

Project: WRXClockPodMod https://drive.google.com/file/d/0ByGxElIxzv3deE43MzN4OHZIa1k/view
Verion: 2

Relevant thread on ClubWRX.net: http://www.clubwrx.net/forums/tutorials-diy/134423369-clock-pod-mod-subarb-select-monitor-ecu-polling-arduino.html

#Theory of operation

For the most part, Subaru's built prior to 2008 do not have CanBus. There are of course expections, however, the main system to log data from pre-canbus ECU's is the Subaru Select Monitor. This project implements monitoring for several parameters, and then transmitts that data over a canbus.

##Parmeters & CAN-ID's

The following parameters are logged:
* Engine Speed (RPM)  - 0x259 Byte 0 & Byte 1
* Vehicle Speed       - 0x259 Byte 2
* Coolant Temprature  - 0x25A Byte 3
* Throttle Position   - 0x259 Byte 3
* Clutch Switch       - 0x25A Byte 1
* Brake Switch        - 0x25A Byte 0
* Calculated Gear     - 0x25A Byte 2

##Requirements
* Arduino UNO or compatiable.
* 1 Canbus sheild (I have utilized the SK Pang can sheild from Sparkfun)
* 1 Arduino ProtoShield Kit  Sparkfun DEV-07914
* 1 Texas Instruments LM339
* 5 10K resistors
* 1 1K resistor
* hookup wire

##Shield

Create your shield with the parts listed above, as well as the schematici from this repository.


