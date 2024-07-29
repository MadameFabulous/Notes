You cannot be ssh'ed into the same user as you're attempting to connect with. The observed behavior is that after logging in via RDP you are presented with  black window session. You can either log on with the xrdp splash or with the integrated user logon with 'Remote Desktop Connection'.
To resolve this I made a spare user 'xrdp'. I can ssh into the normal user like expected and then rdp into a user to interact with the desktop environment.

## Config Based Solution
https://askubuntu.com/questions/1404245/remote-desktop-from-windows-onto-ubuntu-22-04-takes-me-to-a-xrdp-login-then-a-bl
add 
```
export GNOME_SHELL_SESSION_MODE=kali
export XDG_CURRENT_DESKTOP=kali:GNOME
```
to
```
sudo nano /etc/xrdp/startwm.sh
```
