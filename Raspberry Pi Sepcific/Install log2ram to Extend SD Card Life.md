# Install log2ram to Extend SD Card Life
1. Execute the following:
```
cd
mkdir Gits
cd Gits
git clone https://github.com/azlux/log2ram.git
cd log2ram
chmod +x install.sh
sudo ./install.sh
sudo nano /etc/log2ram.conf
```
2. Change `SIZE=40M` to `SIZE=128M`
3. Save the file (CTRL-X, Y, ENTER)
4. `sudo reboot`
5. To check if it was working, use `df -h`
6. This should show the new disk named **log2ram**