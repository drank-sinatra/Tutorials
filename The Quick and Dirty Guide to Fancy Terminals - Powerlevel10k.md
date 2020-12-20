# The Quick and Dirty Guide to Fancy Terminals - Powerlevel10k

## Preface
This should work in most *X operating systems. It’s been tested on Raspberry Pi OS, Ubuntu 20.x, Manjaro 20.x and macOS Catalina and Big Sur.
> **NOTE:** On macOS, it is recommended to install iTerm2 prior to following this tutorial as it is much more customisable than Apple’s Terminal. It may be downloaded [here](https://iterm2.com/downloads.html).  

## Workflow
1. Open a terminal
2. For any **Debian**-based OS, enter the following commands
```
sudo apt update && apt upgrade -y
sudo apt install -y git zsh powerline zsh-syntax-highlighting
```
3. For any **Arch**-based OS, enter the following command:
```
sudo pacman -Syu git zsh powerline zsh-syntax-highlighting
```
4. For **macOS** enter the following command:
```
brew install zsh zsh-syntax-highlighting
```
5. Enter the following commands:
```
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```
6. For **Linux** enter the following
```
echo "source /usr/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc
chsh -s $(which zsh)
```
7. For **macOS** enter the following:
```
echo "source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc
chsh -s /usr/local/bin/zsh
```
9. Run the command `nano .zshrc`
10. Locate the line containing **ZSH_THEME=**
11. Change the line to read **ZSH_THEME="powerlevel10k/powerlevel10k"**
12. Locate the line containing **DISABLE_UPDATE_PROMPT="true"**
13. Uncomment the line by deleting the **#**
14. Locate the line containing **export UPDATE_ZSH_DAYS=13**
15. Uncomment the line by deleting the **#**
16. Change the line to read **export UPDATE_ZSH_DAYS=1**
17. Locate the line containing **ENABLE_CORRECTION="true"**
18. Uncomment the line by deleting the **#**
19. Locate the line beginning with **plugins=(**
20. Select all text on the line
21. Press **Backspace** to delete the line
22. Copy the following:
```
plugins=(
  git
  sudo
  colored-man-pages
)
```
12. Return to the terminal and paste the copied text
13. Press **CTRL+X** to exit
14. Enter **Y** to save changes
15. Press **Enter**
16. Reboot the computer
17. Open a terminal to verify that changes were successful

## Operations and Maintenance
1. To update Oh My ZSH manually, run the command `omz update`
2. To update Powerlevel10k run the command `git -C $ZSH_CUSTOM/themes/powerlevel10k pull`
