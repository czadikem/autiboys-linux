# Autiboy-Linux Debian 11 Distro

## Autiboy's Debian 11
After install of Debian 11

Connect to network and edit it to auto connect using

`nmtui`

Then run this script
```
wget https://raw.githubusercontent.com/czadikem/autiboys-linux/master/debian/11/debian11-setup.sh
chmod +x debian11-setup.sh
sudo ./debian11-setup.sh
```
After your computer has rebooted Login

Run the following in a Terminal in your Desktop Environment

```./debian11-configure.sh```

Then open Terminator and change prefrences to run

```/home/autiboy/Applications/zellij/zellij-updated.sh```

If installing on USB then run this in terminal

##### https://www.youtube.com/watch?v=2gn-jfcaMLM

```sudo grub-install --removable --recheck --efi-directory=/boot/efi```


## Autiboy's Debian 11 Server
After install of Debian 11 Server

Create autiboy user and change who can SSH into the server
##### https://phoenixnap.com/kb/create-a-sudo-user-on-debian
##### https://linuxhandbook.com/sudo-unable-resolve-host/
##### https://www.tecmint.com/wget-download-file-to-specific-directory/
```
adduser autiboy
usermod -aG sudo autiboy
```

Fix SSH host resolution
```
rm -r /etc/hosts
wget https://raw.githubusercontent.com/czadikem/autiboys-linux/master/debian/11/debian11-server-hosts -P /etc/
mv /etc/debian11-server-hosts /etc/hosts
```

Now change SSH permissions

```
apt install nano -y
nano /etc/ssh/sshd_config
```

Add to bottom of file

```PermitRootLogin no```

Save the file

```reboot now```

Login again as autiboy and run this script
```
wget https://raw.githubusercontent.com/czadikem/autiboys-linux/master/debian/11/debian11-server-setup.sh
chmod +x debian11-server-setup.sh
sudo ./debian11-server-setup.sh
```
After your computer has rebooted Login

Run the following in a Terminal in your Desktop Environment

```./debian11-configure.sh```

Then open Terminator and change prefrences to run

```/home/autiboy/Applications/zellij/zellij-updated.sh```

