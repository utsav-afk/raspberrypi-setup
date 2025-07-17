# raspberrypi-setup
A beginner-friendly Raspberry Pi headless setup guide with SSH access

 Raspberry Pi Initial Setup Guide

Objective
Set up a Raspberry Pi with network access and enable SSH for remote control.


 Requirements

- Raspberry Pi (any model)
- microSD card (16GB+ recommended)
- microSD card reader
- Computer with internet access
- Power supply for the Pi
- Ethernet cable (optional but preferred for first-time setup)
- Internet access (Wi-Fi or Ethernet)

Step-by-Step Instructions
Flash the Operating System
1. Download -Raspberry Pi Imager

2. Insert the microSD card into your computer.

3. Open the Imager:
   - Choose OS → *Raspberry Pi OS (32-bit)*
   - Choose Storage → Select your microSD card
   -  Click settings:
     - Set hostname (e.g.,"Raspberrypi")
     - Enable SSH
     - Set username/password
     - Configure Wi-Fi (SSID + password)
     - Set locale
4.Take the SD card out and insert it again
- create "SSH" file and make sure it is saved as all file not text file(.txt)
-create "wpa_supplicant.conf" and make sure it is also saved as all file. Inside this file paste following:
      country=US
      ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
       update_config=1

    network={
       scan_ssid=1
       ssid="your_wifi_ssid"
       psk="your_wifi_password"
       }
5. Click "Write" and wait until it completes.

 Boot the Raspberry Pi

1. Insert the microSD card into the Pi.
2. Connect power.
3. Wait for it  to boot.

Find Raspberry Pi’s IP Address

-Router Method: Check connected devices (look for"raspberrypi")
- IP Scanner: Use [Advanced IP Scanner] 

4️⃣ Connect via SSH
1. Install [PuTTY](https://www.putty.org)
2. Open PuTTY:
   - Hostname: Enter IP or "raspberrypi.local"
   - Port: "22"
3. Login:
   - Username: "pi"
   - Password: (as set during flashing)
