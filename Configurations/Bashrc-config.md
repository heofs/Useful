# .bashrc 

## Personal
```bash
alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'

export CLICOLOR=1
export LSCOLORS=DxFxCxGxCxexexaxaxdxDx

export PS1="\[\e[1;31m\]-------------------------- \w \n\h : \u -> \[\e[0m\] "
export PS2="| => "

screenfetch -A 'Debian'
```
```bash
export PS1="\[\e[1;31m\]__________________________________    | \w \n| => \[\e[0m\] "
export PS2="| => "

export CLICOLOR=1
export LSCOLORS=DxFxCxGxCxexexaxaxdxDx
#export LSCOLORS=DxFxCxGxBxegedabagaced

alias pip='pip3'
alias cd..='cd ../'                         # Go back 1 directory level (for fast typers)
alias ..='cd ../'                           # Go back 1 directory level
alias ...='cd ../../'                       # Go back 2 directory levels
alias .3='cd ../../../'                     # Go back 3 directory levels
alias .4='cd ../../../../'                  # Go back 4 directory levels
alias .5='cd ../../../../../'               # Go back 5 directory levels
alias .6='cd ../../../../../../'            # Go back 6 directory levels
alias ptfldr='cd Documents/Prog/Python'
alias prfldr='cd Documents/Prog'


alias myip='curl ip.appspot.com'                    # myip:         Public facing IP Address
alias netCons='lsof -i'                             # netCons:      Show all open TCP/IP sockets
alias flushDNS='dscacheutil -flushcache'            # flushDNS:     Flush out the DNS Cache
alias lsock='sudo /usr/sbin/lsof -i -P'             # lsock:        Display open sockets
alias lsockU='sudo /usr/sbin/lsof -nP | grep UDP'   # lsockU:       Display only open UDP sockets
alias lsockT='sudo /usr/sbin/lsof -nP | grep TCP'   # lsockT:       Display only open TCP sockets
alias ipInfo0='ipconfig getpacket en0'              # ipInfo0:      Get info on connections for en0
alias ipInfo1='ipconfig getpacket en1'              # ipInfo1:      Get info on connections for en1
alias openPorts='sudo lsof -i | grep LISTEN'        # openPorts:    All listening connections
alias showBlocked='sudo ipfw list'                  # showBlocked:  All ipfw rules inc/ blocked IPs

screenfetch -N -A 'Scientific Linux'
```

## Server
```bash
export CLICOLOR=1
export LSCOLORS=DxFxCxGxCxexexaxaxdxDx

export PS1="\[\e[1;31m\]-------------------------- \w \n\h : \u -> \[\e[0m\] "
export PS2="| => "

screenfetch -A 'Debian'
```
