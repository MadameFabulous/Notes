
```
#Rustscan Docker Alias - Needed for Cast
alias rustscan='docker run -it --rm --name rustscan rustscan/rustscan:2.1.1'

# Utilities
alias cast.rustscan='rustscan -a $tgt -- -sC -sV -Pn'
alias cast.ping='ping $tgt'
alias cast.nmap='nmap -sC -sV -Pn $tgt'
alias cast.autorecon='sudo autorecon $tgt'
alias cast.ctf='source /home/wright-kali/Documents/ovpn/ctf.sh'

#Bash Shortcuts
alias cast.scry='hd -c|awk '\''{$1=""; print $0}'\''' # command to safely read text from hd
alias cast.tun0='export tun0=`ip a | grep "global tun0" | awk '"'"'{print $2}'"'"' | cut -d"/" -f1`' #gets the tun0 interface if there is one and then trims the output and sets a bash variable

# Wordlists Shortcuts
rockyou=/usr/share/wordlists/rockyou.txt
```
