# Avahi on a Raspberry Pi for Easy Remote Access
1. Install the following packages with `sudo apt install avahi-daemon avahi-utils mdns-scan`
2. Reboot with `sudo reboot`
3. From another machine, test functionality with `ping <hostname>.local` where `<hostname>` is the hostname of the device (the default is raspberrypi)
