## Limbo v5.0.0
  
Rebase with QEMU 5.1.0  
Stability and less virtual disk corruptions  
Fixed scaling problem under vnc portrait mode  
Fixed mouse hold and drag under vnc  
Fixed dsl issue with resizing  
Files are now closed via their file descriptor parcels  
Compiled with Android 29  
Migrated to androidx  
Enabled notification icon for Android 29  
Host forward now accepts format "tcp:hostport:guestport"  
 You will need to change your Host Forward configurations  
Configuration files for different QEMU versions  
  
  
## Known Issues:  	
Mouse acceleration issues in QEMU VNC (see guide for disabling it)  	
Emulated audio is slow  	
  
If you want to follow the guides and setup your OS images you should also install QEMU for Windows and Linux:  	

Qemu with GTK (GUI) for Windows Make sure you download a version with GTK if you want a GUI.  	
Qemu Manager (GUI) for Windows  	

If you have Ubuntu or if you run a Debian based linux distro install from the command line with:   	
> sudo apt-get install qemu  
  
Make sure you read the quickstart guide before you do anything else: [here](https://github.com/limboemu/limbo/wiki/Quickstart)  	
  
  
## Downloads  	
See https://github.com/limboemu/limbo/releases for download binary apks.	
** If you're upgrading to version 4 from version 2 or 3 you have to **uninstall** and do a **fresh install**. Make sure you **export** your virtual machines before you uninstall and then **re-import** them.
  
  
## Tools	
The following android apps are recommended:  	

[Hacker's Keyboard](https://play.google.com/store/apps/details?id=org.pocketworkstation.pckeyboard)
Fully qwerty keyboard compatible with Limbo.

[Turbo Download Manager](https://play.google.com/store/apps/details?id=com.okythoos.android.tdmpro)
Multithreaded Download manager for downloading fast ISOs and virtual hard disks.  

[Juice SSH](https://play.google.com/store/apps/details?id=com.sonelli.juicessh)
SSH Client to use when connecting to your vm with forward port 

[ZArchiver](https://play.google.com/store/apps/details?id=ru.zdevs.zarchiver)
File Extractor for use with compressed images.  

[X-plore File Manager](https://play.google.com/store/apps/details?id=com.lonelycatgames.Xplore)
File Manager with FTP client for sharing files with the virtual machines  

[QEMU](https://www.qemu.org)
for desktop to setup your virtual disk images.	
  
