# Fix Spurious DNS Lookups from Pi-Hole
If the host name of a Raspberry Pi has been changed from default after Pi-Hole has been installed, it may cause spurious DNS lookups where the Pi that is hosting Pi-Hole continuously looks for itself.
1. Enter the command `sudo nano /etc/hosts` in order to edit the hosts file
2. Make the below edits, where [hostname] is the correct hostname of the device:
```
## Comment the below line in order to preserve defaults
#127.0.0.1      localhost

## Add the below line
127.0.0.1       [hostname]
::1             localhost ip6-localhost ip6-loopback
ff02::1         ip6-allnodes
ff02::2         ip6-allrouters

## Comment the below line in order to preserve defaults
#127.0.1.1      raspberrypi
```
3. Save the file (CTRL-X, Y, ENTER)
