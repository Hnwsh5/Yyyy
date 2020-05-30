# Current Release: 4.1.0  
Source Code  
Source Code can be found here: https://github.com/limboemu/limbo  
  
  
Release Notes  
  
* Support for compiling with QEMU 4.0.0 see README.developers for instructions
* VNC is now using a Unix domain socket for local connection
* QMP is now using a Unix domain socket for local connection
* Support for allowing QMP external connections
* Updated download and guide links to github repo
* Added software updates option in settings screen
* Moved legacy file manager option to settings screen
* SDL interface is now default
  
  
***

Known Issues:  
Mouse acceleration issues in QEMU VNC (see guide for disabling it)  
Emulated audio is slow  

  
If you want to follow the guides and setup your OS images you should also install QEMU for Windows and Linux:  
  
Qemu with GTK (GUI) for Windows Make sure you download a version with GTK if you want a GUI.  
Qemu Manager (GUI) for Windows  
  
If you have Ubuntu or if you run a Debian based linux distro install from the command line with:   
> sudo apt-get install qemu  
  
Make sure you read the quickstart guide before you do anything else: [here](https://github.com/limboemu/limbo/wiki/Quickstart)  
  
***

## Downloads  
See https://github.com/limboemu/limbo/releases for download binary apks.
** If you're upgrading to version 4 from version 2 or 3 you have to **uninstall** and do a **fresh install**. Make sure you **export** your virtual machines before you uninstall and then **re-import** them.
﻿
***  

## Tools
The following android apps are recommended:  
[Juice SSH](https://play.google.com/store/apps/details?id=com.sonelli.juicessh) To connect to your vm with forward port  
[Hacker's Keyboard](https://play.google.com/store/apps/details?id=org.pocketworkstation.pckeyboard) Fully qwerty keyboard  
[Turbo Download Manager](https://play.google.com/store/apps/details?id=com.okythoos.android.tdmpro) Download fast large  ISOs and virtual hard disks.  
[ZArchiver](https://play.google.com/store/apps/details?id=ru.zdevs.zarchiver)  File Extractor for use with compressed images.  
[ES File Explorer](https://play.google.com/store/apps/details?id=com.estrongs.android.pop)  File Manager with FTP client for sharing files with the virtual machines    
  
  