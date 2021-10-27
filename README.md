# ESP-Dimmer-Switch
Web based Programmable Dimmer Switch Based on the ESP-M3 8285 Module

Warning working with mains power is dangerous do not build this unless you really know what are doing.  Always Disconnect power before working on it.  
This a real risk a Electrocution! As well a fire.

Software currently supports Dimmer , Relay , and Dual Relay versions of the switch. Switches automaticly discover each other with MDNS to create a page of all switches.

Here is a playlist of all my version so far.
https://youtube.com/playlist?list=PL5GnlzXbSNxN_0DaoBrPkn7FY7Wj2uzeJ

Web pages and configuration files are stored in SPIFFS  you will need the "ESP8266 Sketch Data Upload" plugin found at https://github.com/esp8266/arduino-esp8266fs-plugin to upload the Data files.

On the ESP8285 there is 1M of Flash , the settings I have been using the ESP8295 in Arduino IDE.

![image](https://user-images.githubusercontent.com/11134430/139057101-ac52f8e7-b0ad-4301-b314-d7ab33135125.png)

There is a file wifi.cfg you should update it with your wifi settings prior to upload. 

