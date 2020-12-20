# Install Ungoogled Chromium
## Preface
Ungoogled Chromium is a very fast browser stripped of all Google services to make it as private as possible whilst still providing an optimal experience for web applications that prefer Chrome.

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

- - - -

## Arch-based Distros (x64 Only)
> **NOTE:** Ensure the AUR is enabled  
```
sudo pacman -Syu ungoogled-chromium
```

- - - -

## Fedora
```
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
sudo dnf install chromium-browser-privacy
```

- - - -

## macOS
> **NOTE:** Ensure that Homebrew is installed following this [tutorial](https://github.com/drank-sinatra/Tutorials/blob/master/Install%20the%20Homebrew%20Package%20Manager%20on%20macOS.md)  
```
brew fetch --cask eloston-chromium
brew install --cask eloston-chromium
```