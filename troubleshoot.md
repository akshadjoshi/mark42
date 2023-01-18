**command to fix install (if repositaries are missing)**
```bash

 sudo apt --fix-broken install 

```


```bash
apt --fix-missing install
```

```bash
sudo apt satisfy 
```

```bash
apt list --manual-installed=true  # (to see the packages installed)
```


**if your GUI fails to load in Ubuntu** 

```bash
sudo apt purge gdm gdm3
```
```bash
sudo apt install gdm3 ubuntu-desktop
```
**virtual box error (rc=-1908)**

this error occurs when your mac kernal is upgraded (due to apt upgrade) but the application is running on the previous kernal version 
you need to upgrade the application and install the dependency in order to resolve the error


```bash
sudo apt install virtualbox-dkms 
```

then check the virtual box service

```bash
systemctl status virtualbox.service
```
restart the service

```bash
systemctl restart virtualbox.service
```


**to upgrade a single package**
```bash
--apt list upgradable  # will give you list of packages that can upgraded aka has new version
sudo apt --only-upgrade install <packagename/applicationname/toolname>

# this commands comes to play because sudo apt upgrade is not considered as ideal to use all the time on your pc 
```
 
**if GUI fails in KALI Linux after apt upgrade**

`while installing fresh Kali Linux when you do sudo apt upgrade and restart your pc and it does not load GUI and you can't access CLI also do this`

Press "e" on your keyboard as soon as your grub loader boots kali, what it will do is take you to grub rescue 

Now Cursor 'down' to the line that starts with **"linux /boot/**

Cursor right until the cursor is positioned at the end of the line where it says **quiet** or you can also see something like **quite splash**

Use the backspace key to delete the following characters:

```sh
"ro initrd=/install/gtk/initrd.gz quiet"

OR # can see either of the case

"ro initrd=/install/gtk/initrd.gz quiet splash"
```
Type this 
```bash
 rw init=/bin/bash
```
Press Ctrl and "x" to boot to single mode.

`now you will be prompted with a cli`
 
> uninstall/purge gdm3 
 
 ```bash 
 sudo apt purge gdm3
 ```
 
 ```bash
 sudo tasksel    # select by hitting <SPACE>  press TAB and it will go to OK hit ENTER
 ```
  use following command to change default desktop environment
 
 ```bash 
 sudo update-alternatives --config x-session-manager
```
 Enter correct number which represents corresponding desktop environments don't choose gnome because it created all the problem in the first place
 
 ```bash
 sudo reboot
 or exit     # to restart
 ```
