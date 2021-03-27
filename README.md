# chia-farming

How I set up a my headless Raspberry Pi 4 "RPi" to farm Chia.

## Install Raspbian onto RPi
Link

## Set up RPi to connect to wifi

### Enable ssh
* Put `ssh` into boot folder. Upon reboot, the RPi will be enabled for SSH and the file will be removed from the directory.

### Enable wifi
* Edit `wpa_supplicant.conf` and put in two letter country code, network name, and password.
* Put `wpa_supplicant.conf` into boot folder. Upon reboot, the RPi will connect to the network.

### Make sure it farms after reboot (just in case)
* Put rc.local into /etc/rc.local
* Make it executable `sudo chmod +x /etc/rc.local`

### Log into pi
* `ssh pi@<nameofdevice>.local`
* password is `raspberry`

### Change RPi's name
* Update your RPi's name from `raspberrypi` to whatever you'd like.
* Do it here `sudo nano /etc/hostname`
* and here `sudo nano /etc/hosts`

### Change password
* Default password is `raspberry`.
* `passwd`

### Install chia-blockchain
* https://github.com/Chia-Network/chia-blockchain/wiki/Raspberry-Pi

### Mount external drives
* Create mount point
* https://www.raspberrypi.org/documentation/configuration/external-storage.md
