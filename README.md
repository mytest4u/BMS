# China Akku BMS

Fork from https://github.com/mytest4u/BMS

> **Warning**
> Use at your own risk, especially the firmware!

## Links
* [Cerbo GX: VE.Can to CAN-bus BMS cables manual](https://www.victronenergy.com/live/battery_compatibility:can-bus_bms-cable)
* [Venus OS on Pi: CAN Interfaces](https://github.com/victronenergy/venus/wiki/RaspberryPi-CAN-Interfaces)
* [dbus-serialbattery issue,  Support BMS DR-JC03](https://github.com/Louisvdw/dbus-serialbattery/issues/327)

## [Documentation and Manuals](Docs) of the Akku
* DipSwitch, Reset...
* [Guidance - How To Communicate With Upper Computer.pdf](Docs/Guidance%20-%20How%20To%20Communicate%20With%20Upper%20Computer.pdf)

## [DR Software](DR_Software) - Reading data/Firmware Upgrade Tool
* Set address to 0
* Password: 666666

## [Firmware](Firmware)

#### How to update the firmware
1. Connect the PC and battery using a cable, ensuring that DIP 1 is turned ON for PC connection.
2. Make sure to install the necessary RS485 drivers for the connection to be established.
3. Open the "DR-Application.exe" application and keep the window open.
4. Open the "index.html" file located in the "dist" folder using a web browser.

5. On the "Help" tab, change the language to English and enter the password 666666 if prompted.

6. In the "Settings" tab, select the "Update" option, choose the bin file, and initiate the flashing process (you will know it's working if the green LED on the battery is flashing).

#### Victron connection instructions
1. Connect the master pack with DIP 5 and 6 facing upwards, as indicated in the Victron connection instructions.
2. The pack will be recognized as an "LFP battery" and you can view the voltage of the highest and lowest cell under the "Details" section.
3. You can also see the number of packs online and if there's a pack preventing charging/discharging.
4. When DIP 6 is facing upwards, it's recognized as a "Pylontech" Multiplus, and the charge controller will not charge the battery, so avoid using this mode.

### Firmware Files (gladly PR new ones)
* [`DR01_16S100JC03_V2 0 0_T1_V`](Firmware/DR01_16S100JC03_V2%200%200_T1_V.bin) - The V in the file stands for Victron
```
Product info 2.2
Hardware model T1_G
Product model JC03
Project code 16S100
Software version 2.01
Boot version 1.1
```

* [`48V100AH`](Firmware/48V100AH.bin) - also detects the 120AH battery version
```
Product info 2.2
Hardware model T1_V
Product model DR01
Project code 16S100JC03
Software version 2.0.0
Boot version 1.1
```