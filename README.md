## PULSOMETER
<p align="center">
  <img width="600" height="500" src="https://github.com/aritzmaeso/Pulsometer/blob/main/Images/Erlojua%20bukatua.jpg">
</p>

<p align="center">1. Pulsometer

We are students of Electronic Mainetenace who come from Don Bosco.

This proyect consist in building a portable clock heart rate monitor with Attiny85 in a Flexible solder board. Using a MAX30102 sensor to catch the Heart rates, a SSD1306 128x64 OLED display and a LiPo battery of 3,7V. This should **not be used for medical purposes**.
The project is a challenge in software, hardware and soldering.

## Software
**Needed library**

Firstilly, it is important to put attention on the Arduino actualitation, the correct option is **Arduino 1.8.13**. 

In order to build this to the ATTiny85 (In this case we choose it because we do not have enaught space to put the arduino inside the watch) you will need to install the library ATTinyCore.
To install this library, you need to open Arduino IDE, Go to File->Preferences-> Additional Boards Manager URLs Tools. There you easily copy and paste this Link  
https://raw.githubusercontent.com/damellis/attiny/ide-1.6.x-boards-manager/package_damellis_attiny_index.json **This one is to burn the Attiny Chip ( Necessary burn 1 time)**
http://drazzy.com/package_drazzy.com_index.json **This will be to upload the program to the Chip.**

Once you insert the links on the board, you are ready to install the libraries to upload the arduino program to the Attiny Board. You will need to search At Tools-> Board->Boards Manager. There search and install **Attiny85 by Davis** to burn the arduino and **ATTinyCore by Spence Konde** To upload the program to the chip. If we have done the previus steps, we will have 2 new board to choose were upload our program.


<p align="center">
  <img width="600" height="500" src="https://github.com/aritzmaeso/Pulsometer/blob/main/Images/libraries.PNG">
</p>

<p align="center">2. Libraries
 

## Hardware
This is the system on a protoyping board: 

<p align="center">
  <img width="600" height="500" src="https://github.com/aritzmaeso/Pulsometer/blob/main/Images/Protoboard.jpg">
</p>

<p align="center">3. All connected


## Final function
Here you can see the pulsometer working. 
<p align="center">
  <img width="600" height="500" src="https://github.com/aritzmaeso/Pulsometer/blob/main/Images/reloj%20funcioando.png">
</p>

<p align="center">4. Pulsometer working
Now that you have a readed the general explanation go to **"Wiki"** to know how to program at the [ATtiny85](https://github.com/aritzmaeso/Pulsometer/wiki/Arduino-and-ATtiny85), the use of the [Voltera](https://github.com/aritzmaeso/Pulsometer/wiki/PCB-board-at-Voltera) and [3D design](https://github.com/aritzmaeso/Pulsometer/wiki/3D-design) step by step. 




 
 
 




