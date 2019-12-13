# My Ubuntu Configs

### 1. Move Home Folder to HD
- Follow the instructions provided by [Maketecheasier](https://www.maketecheasier.com/move-home-folder-ubuntu/)

### 2. Change Login Background
- Download [here](http://getwallpapers.com/collection/mac-os-yosemite-wallpapers)

```bash
sudo gedit /usr/share/gnome-shell/theme/gnome-shell.css
```

- Change the following lines:
```css
#lockDialogGroup {
  background: #41494c url(resource:///org/gnome/shell/theme/noise-texture.png);
  background-repeat: repeat; }
```

- To:
```css
#lockDialogGroup {
  background: #000000 url(file:///PATH_TO_BACKGROUND/BACKGROUND.PNG);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; }
```

### 3. Change Ubuntu Colors
```bash
sudo gedit /usr/share/gnome-shell/theme/gdm3.css
```

- Change colors: 
```
#e95420 > #501b4d
```

- Change to the color that fits the most with the wallpaper. (Light > #63cde0 > #2a9eb3 > #1c7f91 > Dark)

- Ubuntu color palette [here](https://design.ubuntu.com/brand/colour-palette/).

- RGB finder [here](https://www.w3schools.com/colors/colors_rgb.asp).


### 4. Change dock
#### Install Planck Dock
```
sudo apt-get install plank
```
#### Remove Ubuntu Dock
- Rename /usr/share/gnome-shell/extensions/ubuntu-dock@ubuntu.com to /usr/share/gnome-shell/extensions/ubuntu-dock@ubuntu.com.bak
- Alt + F2
- Type r
- Enter

### 5. Change Terminal Appearance

### 6. Install Main Programs
- Calibre
```bash
sudo -v && wget -nv -O- https://download.calibre-ebook.com/linux-installer.sh | sudo sh /dev/stdin
```
- Chrome ([Download link](https://www.google.com/intl/en-US/chrome/))
- Gimp
```bash
sudo apt-get install gimp
```
- Git
```bash
sudo apt-get install git
git config --global user.name "nome aqui"
git config --global user.email "email aqui"
```
- Java JDK
```bash
sudo apt-get install default-jdk
```
- Netbeans IDE ([Download link](https://netbeans.apache.org/download/))
- RStudio ([Download link](https://www.rstudio.com/products/rstudio/download/))
- Skype
```bash
wget https://go.skype.com/skypeforlinux-64.deb
sudo apt install ./skypeforlinux-64.deb
```
- Spotify
```bash
sudo snap install spotify
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
- Visual Code
```bash
sudo snap install code --classic
```
- Whatsdesk
```bash
sudo snap install whatsdesk
```
### 7. Update drivers
```bash
sudo add-apt-repository ppa:graphics-drivers
sudo apt-get update
sudo apt install nvidia-driver-440
sudo apt autoremove
sudo apt-get upgrade
```

In case of erros regarding public keys, follow [this link](https://chrisjean.com/fix-apt-get-update-the-following-signatures-couldnt-be-verified-because-the-public-key-is-not-available/)'s instructions

### 8. Configurate the Keyboard
- Set "English (US,intl.,with dead keys)
- Edit /etc/environment
```bash
sudo nano /etc/environment
```
- Include: 
```bash
GTK_IM_MODULE=cedilla
```
