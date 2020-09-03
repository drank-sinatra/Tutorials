# Static IP for Pi
## 4.
 Within this file, enter the following lines.
First, you have to decide if you want to set the static IP for your “**eth0**” (Ethernet) connector or you “**wlan0**” (WiFi) connection. Decide which one you want and replace “**<NETWORK>**” with it.
Make sure you replace “**<STATICIP>**” with the IP address that you want to assign to your Raspberry Pi. Make sure this is not an IP that could be easily attached to another device on your network.
Replace “**<ROUTERIP>**” with the IP address that you retrieved in **step 1** of this tutorial
Finally, replace “**<DNSIP>**” with the IP of the domain name server you want to utilize. This is either the IP you got in **step 2** of this tutorial or another one such as Googles “**8.8.8.8**” or Cloudflare’s “**1.1.1.1**“.
interface <NETWORK>
static ip_address=<STATICIP>/24
static routers=<ROUTERIP>
static domain_name_servers=<DNSIP>
Now save the file by pressing **CTRL + X** then **Y** followed by **ENTER**.
## 5.
 Now that we have modified our Raspberry Pi’s DHCP configuration file so that we utilize a static IP address, we need to go ahead and restart the Raspberry Pi.
Restarting the Raspberry Pi will allow our configuration changes to be loaded in and the old ones flushed out.
Upon rebooting, the Raspberry Pi will attempt to connect to the router using the static IP address we defined in our “**dhcpd.conf**” file.
Run the following command to restart your Raspberry Pi.
sudo reboot