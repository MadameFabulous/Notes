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
```
curl -sS https://raw.githubusercontent.com/ajeetdsouza/zoxide/main/install.sh | bash
```
add 
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

