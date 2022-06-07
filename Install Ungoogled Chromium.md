# Install Ungoogled Chromium
## Preface
Ungoogled Chromium is a very fast browser stripped of all Google services to make it as private as possible whilst still providing an optimal experience for web applications that prefer Chrome.

https://github.com/Eloston/ungoogled-chromium

- - - -

## Linux
The best way to install Ungoogled Chromium is through Flatpak. Although there are distribution-specific installers, they are not kept as up-to-date as the Flatpak which is not a good idea from a security perspective.

> **NOTE:** Ensure that Flatpak is installed by following the appropriate setup guide here: https://flatpak.org/setup/

```
flatpak install flathub com.github.Eloston.UngoogledChromium
```

- - - -

## macOS
> **NOTE:** Ensure that Homebrew is installed following this [tutorial](https://github.com/drank-sinatra/Tutorials/blob/master/Install%20the%20Homebrew%20Package%20Manager%20on%20macOS.md)  
```
brew install --cask eloston-chromium
```
