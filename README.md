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


PWM Fan / Ubuntu
----------------

sudo vi /boot/firmware/config.txt

[pi4]
```
dtoverlay=gpio-fan,gpiopin=18,temp=60000

```
eth0 Configuration
---------------------

![Screenshot 2025-04-20 091857](https://github.com/user-attachments/assets/86a4c3ed-87bd-4941-894b-5edd9f8563e2)

Install dhcp client daemon to requset for eth0 ip address:
```
sudo apt-get install dhcpcd5
sudo systemctl enable --now dhcpcd
```

Raspberry Pi no longer uses /etc/network/interfaces -> **auto wlan0** kind of configuration, instead uses wpa_supplicant for WiFi interfaces.

