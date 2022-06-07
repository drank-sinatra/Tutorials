Change a Pi's Screen Brightness

You can vary the brightness by setting a value of 1 to 255 into the file `/sys/class/backlight/rpi-backlight/brightness`.

Example:
```
sudo sh -c "echo 80 > /sys/class/backlight/rpi_backlight/brightness"
```