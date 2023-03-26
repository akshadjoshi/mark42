## multi gesture  in Kali Linux  

<B>`To get multi-gesture functionality on the trackpad in Kali Linux, you need touchegg tool `
  </B>
  
 You don't get the tool in repo so you need the download the `.deb` package via its [github releases](https://github.com/JoseExposito/touchegg/releases)  

 Once you have **downloaded** the package install it. (there are **2 ways to install** the *package*)
 
- by **dpkg**

```bash
sudo dpkg --install ./touchegg_2.0.14_amd64.deb


#   ./(package name) will work only if you are in the folder/directory where the package is downloaded

# you might not get the relevant dependencies need for the package to work properly for that type:
```
```bash
sudo apt --fix-broken install
```
- by **apt**

```bash
sudo apt install ./(downloaded package of touchegg)

# if you will install the package via apt it will automatically install the dependencies required for the package 
```

**check the status of the service and start it**

```bash
systemctl status touchegg.service
```
```bash
systemctl start touchegg.service
```
**enable the service**

```bash
systemctl enable touchegg.service
```

**for the tool to work you need [GNOME shell integration](https://chrome.google.com/webstore/detail/gnome-shell-integration/gphhapmejobijbbhgpjhcjognlahblep) on your browser**

Add the extention to your browser and open the extenstion search for [X11](https://extensions.gnome.org/extension/4033/x11-gestures/) `toggle it to ON`
<B>
  
`it will prompt you to install the extention approve it`
</B>

restart your laptop, after restart try 3 fingure gesture to zoom out of the screen.

can also customize the gestures accordingly in my opinion default just work fine.




## Right click not working in trackpad

`when you install Kali Linux sometimes you come across a weird issue regarding the trackpad
RIGHT click doesn't work as intended i.e. It does not show you the dialog box of copy,paste etc (the one by which you used to refresh your windows PC with)`

to bring it back:

```bash
sudo apt update
```
```bash
sudo apt-get install xserver-xorg-input-synaptics
```

```bash
synclient tapbutton1=1
```
**restart you laptop**

# troubleshoot if synclient keeps on resetting after restart

```bash
Section "InputClass"
    Identifier "touchpad catchall"
    Driver "synaptics"
    MatchIsTouchpad "on"
    Option "PalmMinZ" "100"
    Option "PalmMinWidth" "1"
    Option "PalmDetect" "1"
EndSection
```






