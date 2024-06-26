# Stabilize Shell
```
python3 -c 'import pty;pty.spawn("bin/bash")'
```
```
script /dev/null -c bash 
```
# Concatenate All Files in a Directory Recursively

```
find . -type f -exec cat {} \;
```
# Check how long processes take to start
```
systemd-analyze blame
```
# Check logons
```
: cat /etc/passwd | awk -F : '{print $7}' | sort | uniq
```
# Check if the system is virtualized
```
systemd-detect-virt
```
# Check open ports
```
ss -ntulp | awk '{print $5}' | awk -F : '{print $2}' | sort | uniq
```

# Check Sudo Permissions for SomeUser
```
sudo -l -U SomeUser
```

# Display users on a system
```
awk -F: '{ print $1}' /etc/passwd
```


```
curl -L hotdogstand.lol
```