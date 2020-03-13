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

A.Upgrade to the latest firmware
----------

1.Upgrade Chameleon AVR Firmware

(1)Prepare your Windows computer. Linux or MAC please refer to GITHUB.

(2)Prepare the firmware. Go to GITHUB to compile the latest firmware:
https://github.com/RfidResearchGroup/ChameleonMini Or use the firmware in attachment.

(3) Install the DFU driver. The DFU driver comes from ATMEL's official LIBUSB driver library. You can download it yourself or find it in attachment.

(4)Enter the chameleon DFU mode. When the device is off, press and hold the yellow button near the USB (TINY is the B button), insert the USB, and then you can enter the DFU upgrade mode. Or send the command "UPGRADE" in the connected state, and it can also enter the DFU upgrade mode.

(5)Start to upgrade the firmware. Run the "ChameleonFirmwareUpgrade.bat" file in the attachment to automatically start the firmware upgrade. It usually takes 2-5 seconds. After the progress bar is complete, the firmware upgrade is complete!

(6) A description of the firmware. The chameleon REV.G version uses the same firmware for both the MINI with Bluetooth version and ITNY. The hardware design of the RF part is exactly the same.
The hardware is also compatible with the official firmware of the KAOS brothers: https://github.com/emsec/ChameleonMini

It should be noted that the Android APP is currently not compatible with the official firmware.

2.Upgrade (OTA) Bluetooth firmware for Chameleon MINI

(1) Prepare Android phone and install APP.
Google Store: https://play.google.com/store/apps/details?id=com.proxgrind.chameleon&hl=en
Weiyun download:https://share.weiyun.com/5g1cB6G
Baidu download: https://pan.baidu.com/s/1GqO35IUvFR3kJFwXtCWZiw
Password: e4g1

(2)Open the app and connect the device using Bluetooth. Press any button on the MINI, and the white battery light is on, and Bluetooth is connectable. At this time, open the app again and click Connect to automatically connect the chameleon.

(3) Start upgrade (OTA) Bluetooth firmware. In the “Device Information” column, press “BLE CMD Version” 5 times.
It will pop up the OTA upgrade page, click "Auto Upgrade", and the APP will immediately start to upgrade the latest Bluetooth firmware that comes with it. Automatically exit after the upgrade is complete.

B. Quick Crash Course
----------

1.Detect keys and upload card files

(1) Prepare the computer GUI or Android APP.
 
Computer GUI download address: http://www.icesql.se/download/ChameleonMiniGUI/publish.htm

Source: https://github.com/iceman1001/ChameleonMini-rebootedGUI

Android APP download address:

Google Store:https://play.google.com/store/apps/details?id=com.proxgrind.chameleon&hl=en

Weiyun download: https://share.weiyun.com/5g1cB6G

Baidu download: https://pan.baidu.com/s/1GqO35IUvFR3kJFwXtCWZiw

Password: e4g1

(2) Connect the Chameleon MINI or TINY using the Android APP.

USB port direct connection: Both the Chameleon MINI and TINY support direct connection to the mobile phone USB port. For the MINI, an additional OTG adapter needs to be purchased. TINY uses its own dual-headed TYPEC data cable to connect directly to TYPEC mobile phones.
Bluetooth connection: Chameleon MINI has built-in Bluetooth BLE4.0. Press any button first to wake up Bluetooth. Turn on Bluetooth on your Android phone and the app will automatically connect.

(3)Use Android APP to enable detection mode.

   After connecting, click on a single card slot and select DETECTION_1K or 4K in the "card slot mode". This card slot has the detection mode turned on. Write the original card number in the "UID Card Number" column. Click "Write." If you don't know the UID number, you can fill in it at will. Then click the "Clear" button below to clear the last detection record.

(4)Use Android APP to get keys.

At this time, take the chameleon to the access control reader and swipe. The key and access traces when the chaser reads the chameleon will be recorded by the chameleon.
. At this time, connect back to the mobile phone and click the "crack" button. After few seconds, the app will automatically solve and list the results, as shown in the figure below:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/SKZxgck/Untitled-1.png" alt="Untitled-1" border="0"></a>

The list shows which blocks the read head just visited, and what password was used for each access.
At this point, click the "History" button, the APP will automatically list the keys separately and copy it automatically for easy copying to other software for next use.
If your mobile phone comes with NFC function, you can directly put the original card on the mobile phone NFC at this time, the APP will automatically use the key in the list to read the entire card, and after successful, it will automatically save the entire card data file on the mobile phone. .
Note: Multiple red LEDs are on at the same time during detection, which means the memory is full, just clear the memory.

(5)Use Android APP to import existing card data files in batches.

 Use QQ to send the card data file to the mobile phone QQ, or connect the mobile phone to the computer and transfer the file to any directory on the mobile phone.
Open the app, click the "DUMP" column below, click the "SCanner" in the "plus sign" in the upper right corner, click the three horizontal line buttons in the upper left corner, and select this phone. Then select the root directory of the QQ receiving file or the previously copied directory, and click Allow Access. All card data files will be automatically scanned into the "DUMP file" interface, which can be uploaded or edited at will. 

Click the card data file in the “DUM” column below, and click “Upload” below to upload to the card slot corresponding to the chameleon.

2. Introduction to UID mode and SAK mode

(1)UID mode

After the UID mode is turned on, the card simulated by Chameleon will become a GEN1a card, commonly known as a UID card, Chinese magic card.
Global card slot takes effect.
How to open: Click the button "UID Changeable (GEN1a)" in the APP or directly send the command "UIDMODE = 1" to turn it on, and "UIDMODE = 0" to turn it off.

(2)SAK mode

After the SAK mode is turned on, the card will feedback the real SAK value when it is being found. The SAK value is determined by the 0 sector and 0 block, and the position is the position of the sixth byte immediately after the UID number. If the SAK mode is not turned on, the SAK is a fixed value of 08, and 0 blocks of data are ignored.
This function is used to meet the situation that some cards with special SAK values cannot be used normally after being copied, and can achieve better compatibility.
The current card slot takes effect.
How to open: Click the "SAK Mode" button in the APP or directly send the command "SAKMODE = 1" to turn it on, and "SAKMODE = 0" to turn it off.

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

Parameter
------------------------
Battery Type: LIR2032h rechargeable lithium ion battery  
Charging Tim: 2 hours @ 0-100%  
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

External Contributions
----------------------
Iceman  
Philippe Teuwen  
Willok  
DXL  
ProxGrind aka Olaf  
