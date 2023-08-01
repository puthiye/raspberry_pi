# raspberry_pi

Boot from USB
----------------
1. Raspberry Pi Imager - click the CHOOSE OS button. Next, go to category Misc utility images → Bootloader
2. Select USB Boot – Boot from USB if available, otherwise boot from SD Card.
3. Write the bootloader image to the SD card
4. Disconnect the power supply from your Raspberry Pi
5. Insert the SD card into its slot on the Raspberry Pi, power up
6. The bootloader image now boots and writes your newly configured boot code to the EEPROM chip. (This will enable usb boot)
7. When the ACT led keeps blinking, power down
8. Now write the OS image to USB stick, and connect to Raspberry Pi
