# Wake-On-ESP32
Using an ESP32 to control multiple PCs via Ethernet.

Since WOL (Wake on LAN) was unreliable for me in some use cases and in bulk utilizes to much idle power I build my own system:

![lineup_HD](https://github.com/pixelwave/Wake-On-ESP32/assets/19491804/33a46f0b-b632-4d54-8717-afaebc8437ef)

![Server_Reck_2024-Jan-10_07-31-08AM-000_CustomizedView20343652118](https://github.com/pixelwave/Wake-On-ESP32/assets/19491804/bfc78bb4-148b-4e71-9d82-ec4dc23af22a)

![2024-01-04_awugsy4z56uo](https://github.com/pixelwave/Wake-On-ESP32/assets/19491804/fdf74cb2-8742-47aa-927e-fa609d6f9683)

You choose between a 5 (Standard) or 10 (PRO) port enclosure. WiFi connection or Ethernet (POE). Total Power Consumption is below 1 Watt.

The ESP32 controller is flashed with ESPHome and integrated into my Home Assistant setup for further automation and remote control:

<img width="501" alt="Screenshot 2024-01-04 at 09 27 07" src="https://github.com/pixelwave/Wake-On-ESP32/assets/19491804/090095f4-51db-453c-ae6c-5c5cf84123a4">

The system connects to standard mainboard F_PANEL pins and supports _< shortpress >_ and _< longpress >_ behavior of the power button. Additonally it reads directly the Power LED state. The PCIe card has additional inputs for the standard power button and LED pins from the PC enclosure so you can use both - remote and local control. 

**Wireing (PRO Version)**
![WOESP32-Pro-POE](https://github.com/pixelwave/Wake-On-ESP32/assets/19491804/a4989e78-f4bb-4191-9037-2a1411423622)

**Components**

**PRO Version (POE):**
- 1x Lilygo T-ETH-Lite S3 + POE Shield
- 14x PC817 Optocoupler
- 14x 1K resistors
- 7x Keystone: deleyCON CAT6a (self-wire)
- 1x Keystone: deleyCON CAT6a (direct-plug)
- 1x Keystone: USB-C
- 1x Microswitch (SS-12D00 3Pin 2 Positions 0,5A 50V DC)

**Standard Version (WiFi):**
- 1x ESP32-C3-DevKitM-1
- 8x PC817 Optocoupler
- 8x 1K resistors
- 4x Keystone: deleyCON CAT6a (self-wire)
- 1x Keystone: USB-C

**PCIe Card:**
- 1x Keystone: deleyCON CAT6a (self-wire)
- 1x 4Pin Dupont
  
**3D Model files:**
- **WOESP32 PRO** (10P)
(https://makerworld.com/en/models/122595, https://www.printables.com/model/706094-10p-keystone-enclosure)
- **WOESP32** (5P)
(https://makerworld.com/en/models/122594, https://www.printables.com/model/706089-5p-keystone-enclosure)
- **WOESP32 PCIe Card**
(https://makerworld.com/en/models/95323#profileId-101686, https://www.printables.com/model/679291-pcie-card-adapter-rj-45-keystone-to-2x-4-pin-dupon)

_______
If you like my uploads buy me a coffee -> https://bit.ly/pwave-donate
