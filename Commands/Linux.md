# Linux

## Service commands.
service --status-all
service programName status      # status/start/stop/reload/restart/

#### Disable autostart
sudo update-rc.d servicename disable
sysv-rc-conf                    # Checkboxes alternative.

#### Add username to dialout group for serial access.
sudo usermod -aG dialout YOUR_USERNAME