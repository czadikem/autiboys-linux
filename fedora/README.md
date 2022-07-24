# Autiboy-Linux Fedora Distro

## Autiboy's Fedora
After install of Fedora run this script to install all the apps
```
wget https://raw.githubusercontent.com/czadikem/autiboys-linux/master/fedora/fedora36-setup.sh
chmod +x fedora36-setup.sh
sudo ./debian36-setup.sh
```
Then after the computer reboots login
1. Launch blender and set it up.  Then close it
2. Launch VSCodium and set it up.  Then close it.
```

wget https://raw.githubusercontent.com/czadikem/autiboys-linux/master/fedora/fedora36-configure.sh
chmod +x fedora36-configure.sh
./fedora36-configure.sh
```
Then after the computer reboots again you need to setup gnome
1. Install gnome-sync from extension manager
2. configure it to point to /home/autiboy/Applications/gnome-sync/gnome-sync.json
3. delete the /home/autiboy/.config/gnome-sync.json file
4. launch VSCodium and do the following
1. ```set gitlab token```
2. ```https://gitlab.autiboystech.com```
3. ```ozUa-qtLLAtFhtvmvMgw```