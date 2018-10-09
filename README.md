# My Ubuntu Configs

### 1. Change Plymouth Theme
```
sudo apt-get install plymouth-theme*
sudo update-alternatives --config default.plymouth
sudo update-initramfs -u
```
### 2. Change Login Background
```
sudo gedit /usr/share/gnome-shell/theme/ubuntu.css
```

#### Change the following lines:
```
#lockDialogGroup {
  background: #2c001e url(resource:///org/gnome/shell/theme/noise-texture.png);
  background-repeat: repeat; }
```

#### To:
```
#lockDialogGroup {
  background: #000000 url(file:///PATH_TO_BACKGROUND/BACKGROUND.PNG);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; }
```

### 3. Change dock
#### Remove Ubuntu Dock
```
sudo apt remove gnome-shell-extension-ubuntu-dock
```
#### Install Planck Dock
```
sudo apt-get install plank
```
