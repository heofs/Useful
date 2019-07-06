# Linux

## Services and Processes

`service --status-all` - List all services.

`top` or `htop` - Process management.

`service servicename status` - Alternative arguments `status/start/stop/reload/restart`

## Disks

`sudo fdisk -l` - List all disks.

## Disable autostart

`sudo update-rc.d servicename disable` - Removes service from autostart.

`sysv-rc-conf` - Checkboxes alternative for autostart services.

## Permissions

`sudo chown Username:Groupname` - Add user to new group.

`sudo usermod -aG dialout YOUR_USERNAME` - Add username to dialout group for serial access.

`sudo chown cyrex:cyrex /media/cyrex/party -R` (The R is for recursive so it affects all directory/files and subdirectory.

## Useful packages

`sudo apt-get install exfat-fuse exfat-utils` - Install exfat filesystem driver.

## Verify file checksum

`sha256sum filename` - Returns SHA-256 sum of file.

`md5sum filename` - Return MD5 sum of file.

## Secure delete

`shred -v /dev/sdX` - Add the option -nN to only do this N times.

`shred -vzn 5 file/partition` - Shreds file or partition 5 times. Verbose. Zero last write. n for number of times.

Secure-Delete
srm
smem
sfill
sswap

## Customize settings

`xrandr --output SCREEN1 --output SCREEN2 --output SCREEN3 --same-as SCREEN2` - Extends two screens with one duplicate

`xrandr --output DVI-I-1 --output DVI-D-1 --output HDMI-1 --same-as DVI-I-1`

`env GTK_THEME=Adwaita:light firefox` - Starts program in alternative theme.

## Install .deb package from terminal.

`sudo dpkg -i name.deb`

## SSH

`ssh -i ./private-key.pem user@ipaddress` - SSH to machine using a private key file.

### Setting up SSH keys

1. On server do `ssh-keygen` if keys doesnt exist.
1. Generate a key pair and enter the public key in `~/.ssh/authorized_keys` in one line (needs to start with ssh-rsa).
1. `sudo chmod 700 ~/.ssh`
1. `sudo chmod 600 ~/.ssh/authorized_keys`
1. `sudo chown $USER:$USER ~/.ssh -R`
1. `sudo service ssh restart`
1. Connect to server by specifying your private key matching the public key.
