## Pulsometer
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


 <img width="460" height="300" src="https://gyazo.com/706fa72be212934e64b18e192488baa1">

## Hardware
This is the system on a protoyping board: 
**ARGAZKIA**

The connections needed to make the circuit correctly: 
**Zirkuiton argazkia**


## Step by step

Now that the explanation of the general context it is done, we are going to start step by step. 

### 1st step: Burn the microcontroller

As Attiny85 is a microcontroller, it is necessary an Arduino Uno for the program.
Here it is the datasheet with the connections of the chip. 
**ARGAZKIA**

For the programation you have to put the **Arduino Uno in mode ISP**. 
File->Examples->ArduinoISP and load it. 

Once we have this done, as the Arduino IDE do not support Attiny85 it is needed to develop board. Open File->Preferences->Additional Boards Manager URL; you need to add this URL: https://raw.githubusercontent.com/damellis/attiny/ide-1.6.x-boards-manager/package_damellis_attiny_index.json

Then, we are going to use the libraries that are mentioned in the beginning. Tools->Panel->ATtiny. So now we will start programming the Attiny85 with Arduino Uno as you can see in the image.
**ARGAZKIA konexiokin** We add a capacitor of 10uF between the RESET and GND of the Arduino. This is done so that it does not restart when we upload to the ATtiny85. 

Now, return to the Arduino IDE on Tools->Processor: "ATtiny85" and choose 8MHz (internal) on Tools->Clock.
**ARGAZKIA**


It is important to take into account to have the Arduino as ISP. Tools->Programmer: Arduino as ISP. Have a look again to the other tools, maybe the clock is changed to 1MHz, so put it again in 8MHz.
**ARGAZKIA**

To finish, Tools->Burn Bootloader; to burn the chip. This is only done once for each chip. 
**ARGAZKIA**

To check if all the steps are well done, open Examples->Basics->Blink and change the number 13 to 0. 
**ARGAZKIA** If the program is uploaded correctly you will see "Done uploading". To see it physically, disconnect all the cables and connect them with a Led to see te program in operation. **ARGAZKIA** 

### 2nd step: Upload our program

In the "Arduino program" folder is the program you need to download it and to upload it at the Attiny85. 

Once the program is downoalded, it is necessary to use a new library that it is mentioned at the beggining. Tools->Board->Boards Manager->ATtinyCore. 

When you have the libray: 

 - Tools->Board->ATtinyCore->ATtiny 25/45/85 (No bootloader). 

 - Tools->Chip->ATtiny85.

 - Tools->Clock->8MHz (internal).

 - Tools->Programmer->Arduino as ISP (ATtiny Core).
 
 **NOTE:** To upload a program to the ATtiny85, it is important not to have connected any other component. 
 **ARGAZKIA konektua attiny**

Upload the program and check if in the message it is "Done uploading". 

### 3rd step: Modification of the program

This program is modified to our liking to see it on the dislpay. So you can put what suits you best. 
**ARGAZKIA KAIXO...**

When you have these modifications done, upload it as explained before. 

### 4th step: Connections. 

Since the Attiny85 configurations are done, now we will connect the display and the MAX30102 to the microcontroller. 
**ARGAZKIA DENA KONEKTUA*

Take it into account that the display we have used it is a SSD1306 128x64 OLED so if you have a display with other dimensions you will need to change the coordinates of the words you whant to put. 
**ARGAZKIA HITZEN KORDENADAK**


 
 
 




