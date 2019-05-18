# My Ubuntu Configs

### 1. Change Theme
#### Install Tweak-Tool
```bash
sudo apt install gnome-tweaks
```
#### Set Icons
- Download [MacOS11 icons](https://www.gnome-look.org/p/1102582/) 
- Extract to: ./icons (/home)
- Set "Icons" at Tweak 

#### Set Cursor
- Download [ElCaptain cursor](/OSX-ElCap.zip)
- Extract to: ./icons (/home)
- Set "Cursor" at Tweak

#### Set Theme
- Download [Sierra Light Solid](/Sierra-light-solid.zip)
- Extract to: ./themes (/home)
- Set "Appplications" at Tweak

#### Set Plank Theme
- Download [MacOS Default Color](/macOS-Default-Color.zip)
- Extract to: ./local/share/plank/themes (/home)
- Set "Theme" at Plank (Right-Click at Plank > Preferences)

### 2. Change Plymouth Theme
```bash
sudo apt-get install plymouth-theme*
sudo update-alternatives --config default.plymouth
sudo update-initramfs -u
```
P.S: Pick theme "ubuntu-budgie-logo-scale-2.plymouth"

### 3. Change Login Background
```bash
sudo gedit /usr/share/gnome-shell/theme/gnome-shell.css```

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

### 4. Change Ubuntu Colors
```bash
sudo gedit /usr/share/gnome-shell/theme/gdm3.css
```

### Change colors: 
```
#e95420 > #63cde0
#2c001e > #63cde0
#dd4814 > #63cde0
#e95320 > #63cde0
#dd4814 > #2a9eb3
#bb3e11 > #1c7f91
```

Change to the color that fits the most with the wallpaper. (Light > #63cde0 > #2a9eb3 > #1c7f91 > Dark)

Ubuntu color palette [here](https://design.ubuntu.com/brand/colour-palette/).

RGB finder [here](https://www.w3schools.com/colors/colors_rgb.asp).


### 5. Change dock
#### Remove Ubuntu Dock
```
sudo apt remove gnome-shell-extension-ubuntu-dock
```
#### Install Planck Dock
```
sudo apt-get install plank
```

### 6. Change Terminal Appearance

### 7. Install Main Programs
- Calibre
```bash
sudo -v && wget -nv -O- https://download.calibre-ebook.com/linux-installer.sh | sudo sh /dev/stdin
```
- Chrome ([Download link](https://www.google.com/intl/en-US/chrome/))
- Gimp
```bash
sudo apt-get install gimp
```
- Java JDK
```bash
sudo apt-get install default-jdk
```
- Netbeans IDE ([Download link](https://netbeans.apache.org/download/))
- RStudio ([Download link](https://www.rstudio.com/products/rstudio/download/))
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
- TLP
```bash
sudo add-apt-repository ppa:linrunner/tlp
sudo apt-get update
sudo apt-get install tlp tlp-rdw
sudo tlp start
```
- Virtualbox (Windows with Photoshop)
```bash
yum install VirtualBox-5.2
```
- Yakuake
```bash
sudo apt-get install yakuake
```
