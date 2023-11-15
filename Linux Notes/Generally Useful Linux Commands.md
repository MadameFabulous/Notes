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