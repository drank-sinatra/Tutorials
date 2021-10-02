# Change the Pi Username
1. Login as user pi
2. `sudo nano /etc/ssh/sshd_config`
3. Find the line that begins with `PermitRootLogin` 
4. Edit the line to `PermitRootLogin yes`
5. Press **CTRL+X** to close and save the file
6. Press **Y**
7. Press **Enter**
8. Restart the sshd service using `sudo systemctl reload sshd`
9. Set a root password using `sudo passwd root`
10. Logout using `logout`
11. Login as root using the newly set password
12. Execute `usermod -l <newname> pi` where **newname** is the new username desired to be used
13. Execute `usermod -m -d /home/<newname> <newname>` to rename pi’s home folder to that of the new username
14. Logout using `logout`
15. Login as the new username
16. Execute `sudo passwd -l root` to lock the root user account and prevent unauthorised access
