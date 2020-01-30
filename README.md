Chameleon-Mini
==============
This is NOT the official repository of ChameleonMini, a freely programmable, portable tool for NFC security analysis that can emulate and clone contactless cards, read RFID tags and sniff/log RF data. Thanks to over 1700 backers from our [Kickstarter project](https://www.kickstarter.com/projects/1980078555/chameleonmini-a-versatile-nfc-card-emulator-and-mo), the current Revision G has been realized by Kasper & Oswald GmbH.

Our Project is based on the open-source project by ChameleonMini RevG by Kasper & Oswald [Webshop](https://shop.kasper.it/). 

Our ChameleonMini / ChameleonTiny by ProxGrind is available on Indiegogo now. 
[Done](https://www.indiegogo.com/campaigns/chameleonmini-rev-g-chameleontiny-by-proxgrind/)

Our Asia & Oceania Reseller
[Here](https://sneaktechnology.com/

Our Europe Reseller
[Here](https://lab401.com/)

Our US Reseller
[Here](https://hackerwarehouse.com/)

Most information can be found on [here](http://chameleontiny.com/)

Our APP can be found here: [Here](https://play.google.com/store/apps/details?id=com.proxgrind.chameleon)


Button Usage
-----------
When the power is off, press any button once to turn on the Bluetooth power, and at the same time, display the current power with a white LED.
In the Bluetooth 'ON' state, click any button to turn off the Bluetooth power, the power LED goes out, and the system sleeps.
Bluetooth will sleep automatically 15 seconds after no operation.
Press any button for a long time, you can quickly check the power, and immediately sleep when you release.
Click the button three times to turn on the power of chameleon. Sleep automatically after 5 seconds without operation.
When shutting down, press and hold the button next to USB and then connect USB. You can enter DFU mode.
Charging: Any time you connect USB, it will automatically start charging. Stop automatically after filling. The white LED indicates the power level.
Detect memory full: If the memory is full during dense flow detection, multiple red LEDs will be abnormally lit.

 

Supported Cards and Codecs
--------------------------
See [here](https://github.com/emsec/ChameleonMini/wiki/Supported-Cards-and--Codecs).


Questions
---------
-

External Contributions
----------------------
Iceman  
Philippe Teuwen  
Willok  
DXL  
ProxGrind aka Olaf  

Parameter
------------------------
Battery Type: LIR2032h rechargeable lithium ion battery  
Charging Time: 2 hours @ 0-100%  
Charging Current: 40mA  
Standby Current: 38ma  
Sleep Current: 4uA  
Card Reading Current: 65mA  
Battery Capacity: 70mah  
Usage Time: Use the tag 3 times a day, power on for 5 seconds each time, can use up to one year.  
Port Type: Micro USB (ChameleonMini) / Type-C (ChameleonTiny)  

Repository Structure
--------------------
The code repository contains
* Doc: A doxygen documentation 
* Drivers: Chameleon drivers for Windows and Linux
* Dumps: Dumps of different smartcards
* Hardware: The layout and schematics of the PCB
* Firmware: The complete firmware including a modified Atmel DFU bootloader and LUFA
* Software: Contains a python tool for an easy configuration (and more) of the ChameleonMini, Note that this is currently under construction
* RevE: Contains the whole contents of the discontinued RevE repository.
* RevE-light: Contains our development files for the RevE-light - **WARNING:** currently not supported / not functional
