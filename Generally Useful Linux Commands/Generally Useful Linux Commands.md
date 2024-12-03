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

# Check Users with a Shell
```
cat /etc/passwd|awk -F : '{print $7}'|sort|uniq -c
```

```
cat /etc/passwd|awk -F : '{print $1,"-",$7}'|sort|grep -Ev '/usr/sbin/nologin|/bin/false|/bin/sync'
```
# Print Users 
```
cat /etc/passwd|awk -F : '{print $1,"-",$7}'|sort
```

# Print top 200 largest files
```
du -ah / 2>/dev/null | awk '$1 ~ /[0-9]M/ {print}' | sort -hr|head -200
```

# Search a directory for a file
```
find [directory] -type f -print 2>/dev/null|grep [filename]
```

```
 find / -type f -print 2>/dev/null|grep common.txt
```

# Search a directory for a file or a directory with a specific name
```
find / -print 2>/dev/null|grep common
```
Removing the -type f flag enables the find to hit directories

## Search a directory recursively for SUID files
```
find / -perm -4000 -type f -exec ls -l {} \; 2>/dev/null
```

## Test fstab without reboot
```
mount -a
```
Loads fstab without restart allowing for troubleshooting. Breaking fstab sometimes will prevent you from being able to login to the machine after the daemon restarts.'



# Find TCP Strings from Rustscan
```
grep -oP '\d+/tcp' rustscan-sCV-Pn-T4-p- | sort -u | awk '{print "{" $0 "}"}'
```

