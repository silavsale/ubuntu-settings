# Ubuntu Settings
---
## My notes about Ubuntu settings and applications installation.

* install **GNOME tweaks** from Ubuntu Software center or
from terminal. 
```
sudo apt-get install gnome-tweak-tool
```
* install **Coogle Chrome** from cli 
1. download  

``` wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb ```  

2. install
  
  ``` sudo dpkg -i google-chrome-stable_current_amd64.deb ```

* Check for Update and Upgrade
``` 
sudo apt update
sudo apt upgrade
sudo apt dist-upgrade 
```

* Install Latest Graphics Drivers
Applications Overview >>> Software & Updates >>> Additional Drivers >>> Install/Apply changes

* Third-party Media Codecs & Extras
```
sudo apt install ubuntu-restricted-extras
```
```
sudo apt install libavcodec-extra
```
```
sudo apt install libdvd-pkg
```
* System Cleanup
you can do it in many ways.

You can clean partial packages using a command
```
sudo apt-get autoclean
```
You can auto cleanup apt-cache
```
sudo apt-get clean
```
You can clean up of any unused dependencies
```
sudo apt-get autoremove
```
