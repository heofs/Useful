# ZSH

## Config for ~/.zshrc

```zsh
# vim:ft=zsh ts=2 sw=2 sts=2

# Must use Powerline font, https://github.com/powerline/fonts.
ZSH_THEME_GIT_PROMPT_PREFIX=" -> %{$fg[green]%}\uE0A0 "
ZSH_THEME_GIT_PROMPT_SUFFIX="%{$reset_color%}"
ZSH_THEME_GIT_PROMPT_DIRTY="%{$fg[green]%}!"
ZSH_THEME_GIT_PROMPT_UNTRACKED="%{$fg[green]%}"
ZSH_THEME_GIT_PROMPT_CLEAN="%{$fg[green]%}"

PROMPT='
%{$fg[red]%}%}%~%{$reset_color%}$(git_prompt_info)
%{$fg[red]%}%}%n -> %{$reset_color%}'
```
