# Install Ungoogled Chromium

- - - -

## For Raspberry Pi on Buster
```
echo 'deb http://download.opensuse.org/repositories/home:/ungoogled_chromium/Debian_Buster/ /' | sudo tee /etc/apt/sources.list.d/home-ungoogled_chromium.list > /dev/null
curl -s 'https://download.opensuse.org/repositories/home:/ungoogled_chromium/Debian_Buster/Release.key' | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home-ungoogled_chromium.gpg > /dev/null
sudo apt update
sudo apt install -y ungoogled-chromium
```

- - - -

## For Ubuntu 20.04 Derivatives
```
echo 'deb http://download.opensuse.org/repositories/home:/ungoogled_chromium/Ubuntu_Focal/ /' | sudo tee /etc/apt/sources.list.d/home-ungoogled_chromium.list > /dev/null
curl -s 'https://download.opensuse.org/repositories/home:/ungoogled_chromium/Ubuntu_Focal/Release.key' | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home-ungoogled_chromium.gpg > /dev/null
sudo apt update
sudo apt install -y ungoogled-chromium
```

---

## For Manjaro (x64 Only)

1. Open Add/Remove Software
2. Click the three dots, and choose preferences
3. Enter password as required
4. Click the AUR tab
5. Tick the option for **Enable AUR support**
6. Search for **ungoogled-chromium**
7. Click **Install**