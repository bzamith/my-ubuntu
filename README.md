# My Ubuntu Configs

### 1. Change Theme
#### Install Tweak-Tool
```bash
sudo apt install gnome-tweak-tool
```
#### Set Icons
Download and set [MacOS11 icons](https://www.gnome-look.org/p/1102582/) 

#### Set Cursor
Download and set [ElCaptain cursor](/OSX-ElCap.zip)

### 2. Change Plymouth Theme
```bash
sudo apt-get install plymouth-theme*
sudo update-alternatives --config default.plymouth
sudo update-initramfs -u
```
### 3. Change Login Background
```bash
sudo gedit /usr/share/gnome-shell/theme/ubuntu.css
```

#### Change the following lines:
```css
#lockDialogGroup {
  background: #2c001e url(resource:///org/gnome/shell/theme/noise-texture.png);
  background-repeat: repeat; }
```

#### To:
```css
#lockDialogGroup {
  background: #000000 url(file:///PATH_TO_BACKGROUND/BACKGROUND.PNG);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; }
```

### 4. Change dock
#### Remove Ubuntu Dock
```
sudo apt remove gnome-shell-extension-ubuntu-dock
```
#### Install Planck Dock
```
sudo apt-get install plank
```

### 5. Change Terminal Appearance

### 6. Install Main Programs
- Java JDK
```bash
sudo apt-get install default-jdk
```
- Thunderbird Mail (Package Manager - Ubuntu Store)
- Spotify
```bash
snap install spotify
```
- Sublime
```bash
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo apt-add-repository "deb https://download.sublimetext.com/ apt/stable/"
sudo apt install sublime-text
```
- RStudio ([Download link](https://www.rstudio.com/products/rstudio/download/))
- Python 3 (Pre-installed)
```bash
sudo apt-get update
sudo apt-get -y upgrade
python3 -V
```
- Chrome ([Download link](https://www.google.com/intl/en-US/chrome/))
- Cheese (Package Manager - Ubuntu Store)
- Virtualbox (Windows with Photoshop)
```bash
yum install VirtualBox-5.2
```
- Yakuake
```bash
sudo apt-get install yakuake
```
