# The Quick and Dirty Guide to Fancy Terminals
- - - -
## Preface
This should work in most *X operating systems. It’s been tested on Raspbian Buster and macOS Catalina.

## Workflow
1. Open a terminal
2. Enter the following commands line by line:
```
sudo -s
apt update && apt upgrade -y
apt install git zsh powerline fonts-powerline zsh-syntax-highlighting
exit
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
echo "source /usr/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc
chsh -s $(which zsh)
```
3. Run the command `nano .zshrc`
4. Locate the line containing **ZSH_THEME=**
5. Change the line to read **ZSH_THEME=“agnoster”**
6. Press **CTRL+X** to exit
7. Enter **Y** to save changes
8. Press **Enter**
9. Enter the command `sudo reboot` to reboot your computer
10. Open a terminal

### Additional .zshrc Tweaks
1. Locate the line containing **DISABLE_UPDATE_PROMPT="true"**
2. Uncomment the line by deleting the **#**
3. Locate the line containing **export UPDATE_ZSH_DAYS=13**
4. Uncomment the line by deleting the **#**
5. Change the line to read **export UPDATE_ZSH_DAYS=1**
6. Locate the line containing **ENABLE_CORRECTION="true"**
7. Uncomment the line by deleting the **#**
8. Locate the line beginning with **plugins=(**
9. Select all text on the line
10. Press **Backspace** to delete the line
11. Copy the following:
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
16. Enter the command `exit`
17. Open a terminal to verify that changes were successful

## Operations and Maintenance
1. To update Oh My ZSH manually, run the command `upgrade_oh_my_zsh`
