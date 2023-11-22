OhMyZSH - Automated script for installing ZSH terminals
```
https://github.com/ohmyzsh/ohmyzsh
```


After ohmyzsh reverting root directory reference

https://stackoverflow.com/questions/27885057/zsh-theme-for-full-path-display-git-changes

1. ```echo $ZSH_THEME```
2. ```cp $ZSH/themes/robbyrussell.zsh-theme $ZSH_CUSTOM/themes/ ```
3. ```nano $ZSH_CUSTOM/themes/robbyrussell.zsh-theme```
4. Change %c% to %~% 
   ```PROMPT+=' %{$fg[cyan]%}%c%{$reset_color%} $(git_prompt_info)'``` -> ```PROMPT+=' %{$fg[cyan]%}%~%{$reset_color%} $(git_prompt_info)'```
5. Save the theme, change .zshrc to reference new theme