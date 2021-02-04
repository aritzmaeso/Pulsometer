## Pulsometer
This proyect consist in building a portable clock heart rate monitor with Attiny85 in a Flexible solder board. Using a MAX30102 sensor to catch the Heart rates, a SSD1306 128x64 OLED display and a LiPo battery of 3,7V. This should **not be used for medical purposes**.
The project is an a challengue in software  hardware and soldering.

## Software
**Needed library**
In order to build this to the ATTiny85 (In this case we choose it because we dont have enaught space to put the arduino inside the watch) you will need to install the library ATTinyCore
To install this library you need to open Arduino IDE, Go to File->Preferences-> Additional Boards Manager URLs Tools. There you easily copy and paste this Link  
https://raw.githubusercontent.com/damellis/attiny/ide-1.6.x-boards-manager/package_damellis_attiny_index.json **This one is to burn the Attiny Chip ( Necessary burn 1 time)**
http://drazzy.com/package_drazzy.com_index.json **This will be to upload the program to the Chip.**

Once you insert the links on the board, you are ready to install the libraries to upload the arduino program to the Attiny Board. You will need to search At Tools-> Board->Boards Manager. There search and install **Attiny85 by Davis** to burn the arduino and **ATTinyCore by Spence Konde** To upload the program to the chip. if we have done the previus steps, we will have 2 new board to choose were upload our program 
![](https://gyazo.com/706fa72be212934e64b18e192488baa1")
