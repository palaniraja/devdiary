# Collection of Mac OS X configurations:


### Disable shadows in screenshots

```
defaults write com.apple.screencapture disable-shadow -bool true
killall SystemUIServer
```

### Single window mode:

```
defaults write com.apple.dock single-app -bool true
killall Dock
```

### Show all (hidden) files in Finder

```
defaults write com.apple.Finder AppleShowAllFiles TRUE
killall Finder
```


### Clamshell on Lion/Mountain Lion

  * Disable internal screen - ```sudo nvram boot-args="iog=0x0"```
  * Reenable - ```sudo nvram -d boot-args```


### Finder- Full path in titlebar

```
defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES
killall Finder
```


### Disable Notificationcenter

```
launchctl unload -w /System/Library/LaunchAgents/com.apple.notificationcenterui.plist

killall NotificationCenter

```

**To load again:**
```
launchctl load -w /System/Library/LaunchAgents/com.apple.notificationcenterui.plist
```


### QTKitServer revving my CPU at times, to kill
```
QTKitServer
killall STOP quicklookd
killall STOP QTKitServer
```

### Disable window animations

```
defaults write NSGlobalDomain NSAutomaticWindowAnimationsEnabled -bool false
```


### Seagate/Samsung only Paragon NTFS driver

  * [Seagate Driver](http://www.seagate.com/in/en/support/downloads/item/ntfs-driver-for-mac-os-master-dl/)
  * [Samsung Driver](http://www.seagate.com/in/en/support/downloads/item/samsung-ntfs-driver-master-dl/)