# MP3-TF-16P V3.0
Some tips for using this poor clone of DFPlayer Mini

![img](https://raw.githubusercontent.com/rtek1000/MP3-TF-16P_V3.0/main/MP3-TF-16P_V3.0.jpg)

- 1: Avoid this model. Prefer other models such as the original DFPlayer Mini, MP3-TF-16P (other than V3.0), or try other models (maybe the XY5300 board).
- 2: The module may crash when data is being sent and the microcontroller is reset or reprogrammed. The module may crash if the data sent is not exactly what it should be.
- 3: The RESET command does not work if the module is locked (see tip 2).
- 4: To unlock the module, reset the power (It may be necessary to use a transistor in the power supply). When the power is turned off, a whistle may occur at the audio output (A 3300uF 6.3V capacitor in the supply may help reduce the whistle).
- 5: An interval of around [200ms](https://github.com/ghmartin77/DFPlayerAnalyzer/issues/10) is required between commands (is slower than other models).
- 6: Interval required after RESET command (or power initialization) (maybe 250ms) (LED lights up dimly).
- 7: If the data pins (Busy etc) receive more than 3.3V, it can be passed on to the SD card power supply (It may damage the SD card).
- 8: Command 0x12 (MP3 folder) may not work, try command 0x03 (root directory). The folder must have capital letters (MP3).
- 9: Powering with 5V may cause damage to the SD card and damage to the USBdisk (It no longer recognizes the memories on the computer).
