# OSX Terminal

## Terminal Functionality

```bash
export PS1="\[\e[1;31m\]-------------------------- \w \n\u -> \[\e[0m\] "
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

alias pfolder='cd ~/Documents/Development/Python'
alias dfolder='cd ~/Documents/Development'

alias myip='curl ip.appspot.com'                    # myip:         Public facing IP Address
alias netCons='lsof -i'                             # netCons:      Show all open TCP/IP sockets
alias flushDNS='dscacheutil -flushcache'            # flushDNS:     Flush out the DNS Cache
alias lsock='sudo /usr/sbin/lsof -i -P'             # lsock:        Display open sockets
alias lsockU='sudo /usr/sbin/lsof -nP | grep UDP'   # lsockU:       Display only open UDP sockets
alias lsockT='sudo /usr/sbin/lsof -nP | grep TCP'   # lsockT:       Display only open TCP sockets
alias ipInfo0='ipconfig getpacket en0'              # ipInfo0:      Get info on connections for en0
alias ipInfo1='ipconfig getpacket en1'              # ipInfo1:      Get info on connections for en1


# Setting PATH for Python 3.6
# The original version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.6/bin:${PATH}"
export PATH

neofetch  --block_width 4 --ascii_distro 'Debian'
```

## Terminal Styles

Put in file called custom.terminal and import through mac terminal settings.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>BackgroundColor</key>
	<data>
	YnBsaXN0MDDUAQIDBAUGFRZYJHZlcnNpb25YJG9iamVjdHNZJGFyY2hpdmVyVCR0b3AS
	AAGGoKMHCA9VJG51bGzTCQoLDA0OVU5TUkdCXE5TQ29sb3JTcGFjZVYkY2xhc3NPECcw
	LjE0MTE3NjQ3MDYgMC4xNDExNzY0NzA2IDAuMTQxMTc2NDcwNgAQAYAC0hAREhNaJGNs
	YXNzbmFtZVgkY2xhc3Nlc1dOU0NvbG9yohIUWE5TT2JqZWN0XxAPTlNLZXllZEFyY2hp
	dmVy0RcYVHJvb3SAAQgRGiMtMjc7QUhOW2KMjpCVoKmxtL3P0tcAAAAAAAABAQAAAAAA
	AAAZAAAAAAAAAAAAAAAAAAAA2Q==
	</data>
	<key>Font</key>
	<data>
	YnBsaXN0MDDUAQIDBAUGGBlYJHZlcnNpb25YJG9iamVjdHNZJGFyY2hpdmVyVCR0b3AS
	AAGGoKQHCBESVSRudWxs1AkKCwwNDg8QVk5TU2l6ZVhOU2ZGbGFnc1ZOU05hbWVWJGNs
	YXNzI0AmAAAAAAAAEBCAAoADXU1lbmxvLVJlZ3VsYXLSExQVFlokY2xhc3NuYW1lWCRj
	bGFzc2VzVk5TRm9udKIVF1hOU09iamVjdF8QD05TS2V5ZWRBcmNoaXZlctEaG1Ryb290
	gAEIERojLTI3PEJLUltiaXJ0dniGi5afpqmyxMfMAAAAAAAAAQEAAAAAAAAAHAAAAAAA
	AAAAAAAAAAAAAM4=
	</data>
	<key>ProfileCurrentVersion</key>
	<real>2.0499999999999998</real>
	<key>ShowActiveProcessArgumentsInTitle</key>
	<true/>
	<key>ShowActiveProcessInTabTitle</key>
	<true/>
	<key>ShowActiveProcessInTitle</key>
	<false/>
	<key>ShowActivityIndicatorInTab</key>
	<true/>
	<key>ShowCommandKeyInTitle</key>
	<false/>
	<key>ShowDimensionsInTitle</key>
	<false/>
	<key>ShowRepresentedURLInTabTitle</key>
	<true/>
	<key>ShowRepresentedURLInTitle</key>
	<false/>
	<key>ShowRepresentedURLPathInTabTitle</key>
	<true/>
	<key>ShowRepresentedURLPathInTitle</key>
	<false/>
	<key>ShowShellCommandInTitle</key>
	<false/>
	<key>ShowTTYNameInTitle</key>
	<false/>
	<key>ShowWindowSettingsNameInTitle</key>
	<false/>
	<key>TextColor</key>
	<data>
	YnBsaXN0MDDUAQIDBAUGFRZYJHZlcnNpb25YJG9iamVjdHNZJGFyY2hpdmVyVCR0b3AS
	AAGGoKMHCA9VJG51bGzTCQoLDA0OVU5TUkdCXE5TQ29sb3JTcGFjZVYkY2xhc3NPECcw
	LjkwMTk2MDc4NDMgMC45MDU4ODIzNTI5IDAuNzE3NjQ3MDU4OAAQAYAC0hAREhNaJGNs
	YXNzbmFtZVgkY2xhc3Nlc1dOU0NvbG9yohIUWE5TT2JqZWN0XxAPTlNLZXllZEFyY2hp
	dmVy0RcYVHJvb3SAAQgRGiMtMjc7QUhOW2KMjpCVoKmxtL3P0tcAAAAAAAABAQAAAAAA
	AAAZAAAAAAAAAAAAAAAAAAAA2Q==
	</data>
	<key>columnCount</key>
	<integer>90</integer>
	<key>name</key>
	<string>Custom</string>
	<key>rowCount</key>
	<integer>24</integer>
	<key>type</key>
	<string>Window Settings</string>
</dict>
</plist>
```
