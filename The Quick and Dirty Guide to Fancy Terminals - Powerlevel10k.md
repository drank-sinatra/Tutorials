# The Quick and Dirty Guide to Fancy Terminals - Powerlevel10k

## Preface
This should work in most *X operating systems. It’s been tested on Raspberry Pi OS, Ubuntu 20.x, Manjaro 20.x and macOS Catalina and Big Sur.
> **NOTE:** On macOS, it is recommended to install iTerm2 prior to following this tutorial as it is much more customisable than Apple’s Terminal. It may be downloaded [here](https://iterm2.com/downloads.html).  

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
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
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
8. Run the command `nano .zshrc`
9. Locate the line containing **ZSH_THEME=**
10. Change the line to read **ZSH_THEME=“powerlevel10k/powerlevel10k”**
11. Locate the line containing **zstyle ':omz:update' mode auto**
12. Uncomment the line by deleting the **#**
13. Locate the line containing **zstyle ':omz:update' frequency 13**
14. Uncomment the line by deleting the **#**
15. Change the line to read **zstyle ':omz:update' frequency 1**
16. Locate the line containing **ENABLE_CORRECTION="true"**
17. Uncomment the line by deleting the **#**
18. Locate the line beginning with **plugins=(**
19. Select all text on the line
20. Press **Backspace** to delete the line
21. Copy the following:
```
plugins=(
  brew
  git
  sudo
  colored-man-pages
  zsh-syntax-highlighting
)
```
22. Return to the terminal and paste the copied text
23. Press **CTRL+X** to exit
24. Enter **Y** to save changes
25. Press **Enter**
26. Reboot the computer
27. Open a terminal to verify that changes were successful

## Operations and Maintenance
1. To update Oh My ZSH manually, run the command `omz update`
2. To update Powerlevel10k run the command `git -C $ZSH_CUSTOM/themes/powerlevel10k pull`
