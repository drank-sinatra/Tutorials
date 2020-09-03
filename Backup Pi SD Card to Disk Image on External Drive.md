# Backup Pi SD Card to Disk Image on External Drive
1. SSH to the server you wish to backup
2. Enter the following command, substituting <external_disk_mount> with the name of the external disk to which the image should be saved
 `sudo dd if=/dev/mmcblk0 of=/media/<external_disk_mount>/SDbackup.img bs=4M status=progress`
3. Provided that all completes successfully, a CRON job can be created in order to back the SD card on a scheduled basis
	1. **NOTE:** To get the correct CRON schedule syntax leverage [Crontab Generator](https://crontab-generator.org) 
4. Enter the command `crontab -e`
5. At the end of the file, place the generated syntax
_Example:_
```
# Executes at 0200 every Sunday, outputting to a USB-connected SSD
`0 2 * * 0 sudo dd if=/dev/mmcblk0 of=/media/usbssd/SDbackup.img bs=4M`
```
**NOTE:** The progress option is omitted as the command will be running in the background