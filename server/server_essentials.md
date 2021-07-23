# Server Essentials

## Enable SSH

To connect to your server non-physically set up SSH.

## Set up a new user

Don't use the admin user. If your server has a default user (e.g RPI)
it's recommended to remove that user.

`useradd <user> -s /bin/bash/ -m -G adm, sudo`
`passwd <user>`

`userdel pi`
`rm -rf /home/pi`

## Change hostname

Edit `/etc/hosts` and `/etc/hostname` then reboot
Use SSH-keys to login

### Allow server to be found by hostname

`sudo systemctl status avahi-daemon` Check this is running
If it is, great. The server should connect via `user@host` or `user@host.local`

## Set a static IP

## Enable SSH keys

### Disable password logins
