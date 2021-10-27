# ESP-Dimmer-Switch
Web based Programmable Dimmer Switch Based on the ESP-M3 8285 Module

Of couse the code will work on any esp8266 or esp8255 but it will need at least 1M of flash for OTA to work.

I drew on many sources when I started this project I apologize for not keeping better track to give credit, I know one of many was: https://www.instructables.com/Arduino-controlled-light-dimmer-The-circuit/

Warning!! working with mains power is dangerous do not build this unless you really know what are doing.  Always Disconnect power before working on it.  There a real risk a Electrocution! As well a fire. Build at your own risk. 

Software currently supports Dimmer , Relay , and Dual Relay versions of the switch. Switches automaticly discover each other with MDNS to create a page of all switches.
![image](https://user-images.githubusercontent.com/11134430/139081621-dfff785e-005d-4824-96eb-8abf697a2315.png)


Here is a playlist of all my versions so far.
https://youtube.com/playlist?list=PL5GnlzXbSNxN_0DaoBrPkn7FY7Wj2uzeJ

Web pages and configuration files are stored in SPIFFS  you will need the "ESP8266 Sketch Data Upload" plugin found at https://github.com/esp8266/arduino-esp8266fs-plugin to upload the Data files.

On the ESP8285 there is 1M of Flash , below are the settings I have been using for the ESP8295 in Arduino IDE. Flash size is the only one that matters if you change it from one upload to the next it will wipe out the file system.

![image](https://user-images.githubusercontent.com/11134430/139057101-ac52f8e7-b0ad-4301-b314-d7ab33135125.png)

There is a file, wifi.cfg you should update it with your wifi settings prior to upload. 

The switch are remotely trigger-able with any http client.
 Sample On at 50%
The switch are remotely trigger-able with any http client
Sample On at 50%
 http://10.16.10.172/Activate?st2=1&st3=50

Sample off
 http://10.16.10.172/Activate?st2=0

On for 30secs
 http://10.16.10.172/Activate?st2=4&TA=30


st2=0  off               :none
st2=1 on                 :st3=Dimming 
st2=2 Strobe/Emergency   :none
st2=3 Toggle state       :st3=Dimming 
st2=4 Timed Activation   :TA=Secs

Macros
File /test1.mcr (list of above commands)
 http://10.16.10.172/Macro?MCM=test1


Switch TYPE
0=(on/off) pins(0/2) toggle  ESP8266-1
1=pins 14(trac),4(zero cross) 13(button) ESP-M3 8285
3=Relay(not implemented yet)

Switch Mode
1=No Dim
2=Dim

