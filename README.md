# chia-farming

How to set up an RPi with Raspbian headless.

### Set password

### Change RPi's name

### Enable ssh
* Put `ssh` into boot folder

### Enable wifi
* Put `wpa_supplicant.conf` into boot folder
* Edit `wpa_supplicant.conf` and put in two letter country code, network name, and password.

 
### Make sure it farms after reboot (just in case)
* Put rc.local into /etc/rc.local
* Make it executable `sudo chmod +x /etc/rc.local`

### Log into pi
`ssh pi@<nameofdevice>.local`
