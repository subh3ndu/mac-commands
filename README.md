# Useful MacOS Commands


1. Make Dock Hiding Faster

```
defaults write com.apple.dock autohide-delay -float 0; defaults write com.apple.dock autohide-time-modifier -int 0;killall Dock
```

2. Add Dock Spacer (full)

```
defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="spacer-tile";}' && killall Dock
```

3. Add Dock Spacer (Half)

```
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="small-spacer-tile";}' && killall Dock
```

4. Change Screenshot Default to JPG

```
defaults write com.apple.screencapture type jpg
```

5. Change Default Screenshot folder(mine is downloads folder)

```
defaults write com.apple.screencapture location /Users/sub3ndu/Downloads && killall SystemUIServer
```

6. Make Hidden Apps Transparent

```
defaults write com.apple.Dock showhidden -bool TRUE && killall Dock
```

7. IF anything ugly happens the to reset the dock

```
defaults delete com.apple.dock && killall Dock && killall Finder
```

8. Remove Workspace auto-switching 

```
defaults write com.apple.dock workspaces-auto-swoosh -bool NO && killall Dock
```

9. Disable Disk warning (must restart to take effect)

```
sudo defaults write /Library/Preferences/SystemConfiguration/com.apple.DiskArbitration.diskarbitrationd.plist DADisableEjectNotification -bool YES && sudo pkill diskarbitrationd
```
