### Hi everyone, this is my Ubuntu settings and app's to install guide.

# I Welcome everybody to commit your's settings and apps to this repo.

# Ubuntu Settings
---
## My notes about Ubuntu settings and applications installation.

### install **GNOME tweaks** from Ubuntu Software center or
from terminal. 
```
sudo apt-get install gnome-tweak-tool
```
### install **Coogle Chrome** from cli 
1. download  

``` wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb ```  

2. install
  
  ``` sudo dpkg -i google-chrome-stable_current_amd64.deb ```

### Check for Update and Upgrade
``` 
sudo apt update
sudo apt upgrade
sudo apt dist-upgrade 
```

### Install Latest Graphics Drivers
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
### System Cleanup
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
### Install openweather  form ubuntu software center > add-on

### Remove firefoxsudo
```
apt-get purge firefox
```
### Remove thunderbird
```
sudo apt-get purge thunderbird*
```
* vs code 
```
sudo apt update
```
```
sudo apt install software-properties-common apt-transport-https wget
```
```
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
```
```
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
```
```
sudo apt install code
```

***

### remove mongodb 
In my case `mongodb` packages are named `mongodb-org` and `mongodb-org-*`

So when I type `sudo apt purge mongo` then `tab` (for auto-completion) I can see all installed packages that start with `mongo`.

Another option is to run the following command (which will list all packages that contain `mongo` in their names or their descriptions):

    dpkg -l | grep mongo

In summary, I would do (to purge all packages that start with `mongo`):

    sudo apt purge mongo*

and then (to make sure that no mongo packages are left):

    dpkg -l | grep mongo

Of course, as mentioned by @alicanozkara, you will need to manually remove some directories like `/var/log/mongodb` and `/var/lib/mongodb`

Running the following `find` commands:

`sudo find /etc/ -name "*mongo*"` and `sudo find /var/ -name "*mongo*"`

may also show some files that you may want to remove, like:

    /etc/systemd/system/mongodb.service
    /etc/apt/sources.list.d/mongodb-org-3.2.list

and:

    /var/lib/apt/lists/repo.mongodb.*


You may also want to remove user and group `mongodb`, to do so you need to run:

    sudo userdel -r mongodb
    sudo groupdel mongodb

To check whether `mongodb` user/group exists or not, try:

    cut -d: -f1 /etc/passwd | grep mongo
    cut -d: -f1 /etc/group | grep mongo
***
### install mongodb
```
sudo apt-get install mongodb
sudo apt-get update
sudo service mongodb start
mongo
```
* to see db, run 
```
db
```
&
```
show dbs
```

### user error while installing mongo db fixed 
enter this code 
```
sudo nano /var/lib/dpkg/statoverride
```
then remove existing user.

### donwload and install mongodb compass
https://docs.mongodb.com/compass/master/install/

https://www.mongodb.com/download-center/compass?jmp=docs

##### Download Compass
To download Compass, you can use your preferred web browser.

##### Open the downloads page.
Download the latest version of MongoDB Compass for Ubuntu. The MongoDB Compass installer is a .deb package.
##### Install Compass
Double-click on the .deb package icon to start installation.

##### Click Install.

Once installed, launch Compass from your Applications folder.

##### Start Compass:
```
mongodb-compass
```
