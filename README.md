# chia-farming

How I set up a my headless Raspberry Pi 4 "RPi" to farm Chia.

## Install Raspbian onto RPi
Link

### Update!
`sudo apt update`
`sudo apt upgrade`

## Set up RPi to connect to wifi

### Enable ssh
* Put `ssh` into boot folder. Upon reboot, the RPi will be enabled for SSH and the file will be removed from the directory.

### Enable wifi
* Edit `wpa_supplicant.conf` and put in two letter country code, network name, and password.
* Put `wpa_supplicant.conf` into boot folder. Upon reboot, the RPi will connect to the network.

### Make sure it farms after reboot (just in case)
* Put rc.local into /etc/rc.local
* Make it executable `sudo chmod +x /etc/rc.local`

### Power up the Pi!

### Find its ip
`ping raspberrypi.local`

### Log into pi
* `ssh pi@<ip>`
* password is `raspberry`

### Change password
* Default password is `raspberry`.
* `passwd`

### Change RPi's name
* Update your RPi's name from `raspberrypi` to whatever you'd like.
* Do it here `sudo nano /etc/hostname`
* and here `sudo nano /etc/hosts`
* Reboot to have it take effect `sudo reboot`

### Install chia-blockchain
* https://github.com/Chia-Network/chia-blockchain/wiki/Raspberry-Pi

### Mount external drives
* Create mount point
* https://www.raspberrypi.org/documentation/configuration/external-storage.md


### Chiadog
* Update Python https://linuxize.com/post/how-to-install-python-3-7-on-debian-9/
* Update Pip
* Make sure Requirements installed https://github.com/martomi/chiadog/blob/main/requirements.txt

### Robustness
* set up reboot on network interruption https://weworkweplay.com/play/rebooting-the-raspberry-pi-when-it-loses-wireless-connection-wifi/
* start chia farm on boot https://weworkweplay.com/play/raspberry-pi-nodejs/
* start chiadog on boot
