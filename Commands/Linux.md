# Linux

## Service commands.
service --status-all
service programName status      # status/start/stop/reload/restart/

#### Disable autostart
sudo update-rc.d servicename disable
sysv-rc-conf                    # Checkboxes alternative.

#### Add username to dialout group for serial access.
sudo usermod -aG dialout YOUR_USERNAME

# Useful installations.
sudo apt-get install exfat-fuse exfat-utils         # Install exfat driver.

# Checksums
sha256sum filename
md5sum filename


# Change ownership (chown).
For example sudo chown cyrex:cyrex (User:Group)

if the partition is called party, your user is called cyrex and it is in /media just do for example:

sudo chown cyrex:cyrex /media/cyrex/party -R (The R is for recursive so it affects all directory/files and subdirectory.

# Start program in alternative theme.
env GTK_THEME=Adwaita:light firefox

# List disks
sudo fdisk -l                   # List all disks.
  
# Secure delete alternatives.
## Add the option -nN to only do this N times.
sudo shred -v /dev/sdX

## Shreds file or partition 5 times. Verbose. Zero last write. n for number of times.
shred -vzn 5 file/partition

sudo shred -v -z /dev/sdX

Secure-Delete
    srm
    smem
    sfill
    sswap

# Dual screen two, mirror two.
xrandr --output SCREEN1 --output SCREEN2 --output SCREEN3 --same-as SCREEN2
xrandr --output DVI-I-1 --output DVI-D-1 --output HDMI-1 --same-as DVI-I-1

# Install .deb package from terminal.
sudo dpkg -i name.deb

