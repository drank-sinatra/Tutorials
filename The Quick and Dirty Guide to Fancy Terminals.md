# The Quick and Dirty Guide to Fancy Terminals

## Preface
This should work in most *X operating systems. It’s been tested on Raspberry Pi OS, Ubuntu 20.x, Manjaro 20.x and macOS Catalina and Big Sur.
> **NOTE:** On macOS, it is recommended to install iTerm2 prior to following this tutorial as it is much more customisable than Apple’s Terminal. It may be installed via Brew `brew install iterm2` or downloaded [here](https://iterm2.com/downloads.html).  

## Workflow
1. Open a terminal
2. For any **Debian**-based OS, enter the following commands
```
sudo apt update && sudo apt upgrade -y
sudo apt install -y git zsh powerline
```
3. For any **Arch**-based OS, enter the following command:
```
sudo pacman -Syu git zsh powerline
```
4. For **macOS** enter the following command:
```
xcode-select --install
```
5. Enter the following commands:
```
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
6. For **Linux** enter the following
```
chsh -s $(which zsh)
```
7. For **macOS** enter the following:
```
chsh -s /usr/local/bin/zsh
```
7. Run the command `nano .zshrc`
8. Locate the line containing **ZSH_THEME=**
9. Change the line to read **ZSH_THEME=“agnoster”**
> Other themes can be found [here](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes).
10. Locate the line containing **zstyle ':omz:update' mode auto**
11. Uncomment the line by deleting the **#**
12. Locate the line containing **zstyle ':omz:update' frequency 13**
13. Uncomment the line by deleting the **#**
14. Change the line to read **zstyle ':omz:update' frequency 1**
15. Locate the line containing **ENABLE_CORRECTION="true"**
16. Uncomment the line by deleting the **#**
17. Locate the line beginning with **plugins=(**
18. Select all text on the line
19. Press **Backspace** to delete the line
20. Copy the following:
```
plugins=(
  brew
  git
  sudo
  colored-man-pages
  zsh-syntax-highlighting
)
```
21. Return to the terminal and paste the copied text
22. Press **CTRL+X** to exit
23. Enter **Y** to save changes
24. Press **Enter**
25. Reboot the computer
26. Open a terminal to verify that changes were successful

## Operations and Maintenance
1. To update Oh My ZSH manually, run the command `omz update`
