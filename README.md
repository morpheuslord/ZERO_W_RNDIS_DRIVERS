# ZERO W RNDIS DRIVERS
RNDIS Drivers for Zero w 1.1 

## Usage
### On the PI
- *Step 1:* Add these values within the `/boot/config.txt` remember to add this on the last line
  - ```bash
    dtoverlay=dwc2
    ```  
- *Step 2:* Add these values within the `/boot/cmdline.txt` remember to add this in the last of the file not just after `rootwait`
  - ```bash
    modules-load=dwc2,g_ether
    ```
  - Or else just paste this in the file:
    - ```bash
      console=serial0,115200 console=tty1 root=PARTUUID=5f858bfa-02 rootfstype=ext4 fsck.repair=yes rootwait cfg80211.ieee80211_regdom=GB modules-load=dwc2,g_ether
      ```
- *Step 3:* Run this command: `sudo apt-get install bridge-utils libs3dw2`
- *Step 4:* Reboot: `sudo reboot`

### On Windows
- *Step 1:* Clone this repo `git clone https://github.com/morpheuslord/ZERO_W_RNDIS_DRIVERS`
- *Step 2:* Open the device manager and add these drivers to the network devices.
- *Step 3:* Connect the PI and check connection
