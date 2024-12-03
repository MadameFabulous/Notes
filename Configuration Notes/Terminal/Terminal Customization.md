## Installs
```
sudo apt install zsh
sudo apt install git
sudo apt install curl
sudo apt install neofetch
sudo apt install lolcat
sudo apt install tmux
```

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

OhMyZSH - Automated script for installing ZSH terminals
```
https://github.com/ohmyzsh/ohmyzsh
```

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## After ohmyzsh reverting root directory reference

https://stackoverflow.com/questions/27885057/zsh-theme-for-full-path-display-git-changes

```
echo $ZSH_THEME
```

```
cp $ZSH/themes/robbyrussell.zsh-theme $ZSH_CUSTOM/themes/paxromana.zsh-theme&&nano $ZSH_CUSTOM/themes/paxromana.zsh-theme
```

Change %c% to %~% 
   ```PROMPT+=' %{$fg[cyan]%}%c%{$reset_color%} $(git_prompt_info)'``` -> ```PROMPT+=' %{$fg[cyan]%}%~%{$reset_color%} $(git_prompt_info)'```l;s
5. Save the theme, change .zshrc to reference new theme

7. ```sudo nano ~/.zshrc```
## Update .zshrc file
	Update .zshrc file to reference the new template (paxromana)
```
sudo nano .zshrc
```

![[Pasted image 20240220194452.png]]

## Adding zoxide
['zoxide init --cmd cd bash' causing using cd to crash terminal · Issue #694 · ajeetdsouza/zoxide · GitHub](https://github.com/ajeetdsouza/zoxide/issues/694)

```
curl -sS https://raw.githubusercontent.com/ajeetdsouza/zoxide/main/install.sh | bash
```
## Adding Neofetch and zshrc
```
clear
neofetch|lolcat
eval "$(zoxide init --cmd cd zsh)"
```
to .zshrc
### $PATH Variable issue
Solution
![[Pasted image 20240222003258.png]]
The above note is a callout to check the $PATH

Edit .zshrc, adding the path from the note to the end of the path string in the config. By default it will be commented out when pulling it down from oh-my-zsh initially
![[Pasted image 20240222004733.png]]
Source: ['zoxide init --cmd cd bash' causing using cd to crash terminal · Issue #694 · ajeetdsouza/zoxide · GitHub](https://github.com/ajeetdsouza/zoxide/issues/694)

```
export PATH=/home/{host_name}/.local/bin:$PATH
```

# Autocomplete (Same style as base kali)
```
source /usr/share/zsh-autosuggestions/zsh-autosuggestions.zsh
```

![[Pasted image 20241116145226.png]]


```
NEWLINE=$'\n'
PROMPT="%F{#FFFFFF}$(TZ=America/New_York date "+%H:%M:%S") %F{#5BCEFA}%n@%m %F{#F5A9B8}%~ %f${NEWLINE}%F{#F5A9B8}$(TZ=UTC date "+%H:%M:%S") %F{#FFFFFF}> %f"
```


## Example
```
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
export LANG=en_US.UTF-8
export LC_ALL=en_US.UTF-8

#autosuggetion
source /usr/share/zsh-autosuggestions/zsh-autosuggestions.zsh
#zoxide
export PATH=$PATH:/home/madamefabulous/.local/bin
eval "$(zoxide init --cmd cd zsh)"
#neovim
export PATH="$PATH:/opt/nvim-linux64/bin"

#searchvector
alias searchvector="/opt/searchvector/myenv/bin/python3 /opt/searchvector/searchvector.py"
#siren templates
alias common="clear;cat /home/madamefabulous/Documents/common;tmux set mouse off"
alias shells="clear;cat /home/madamefabulous/Documents/shells;tmux set mouse off"
alias breakout="clear;cat /home/madamefabulous/Documents/breakout;tmux set mouse off"
alias template="clear;cat /home/madamefabulous/Documents/template;tmux set mouse off"


NEWLINE=$'\n'
PROMPT="%F{#FFFFFF}$(TZ=America/New_York date "+%H:%M:%S") %F{#5BCEFA}%n@%m %F{#F5A9B8}%~ %f${NEWLINE}%F{#F5A9B8}$(TZ=UTC date "+%H:%M:%S") %F{#FFFFFF}> %f"
```


Updates every time
```
precmd() {
    NEWLINE=$'\n'
    PROMPT="%F{#FFFFFF}$(TZ=America/New_York date "+%H:%M:%S") %F{#5BCEFA}%n@%m %F{#F5A9B8}%~ %f${NEWLINE}%F{#F5A9B8}$(TZ=UTC date "+%H:%M:%S") %F{#FFFFFF}> %f"
}
```