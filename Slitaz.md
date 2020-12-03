Slitaz Linux is another OS that is compatible with Limbo.  
This is a good option if you want a light weight linux distribution with a 3.x linux kernel and have a high end Android device.

You can download the live ISO from the official website:
http://www.slitaz.org

You can boot directly the live cd with Limbo:
### Limbo Configuration
cpu: x86  
memory: 512  
net: user  
nic: default  
cdrom: slitaz.iso  
  
  
### Slitaz installation to hard disk (optional)
Install Slax on the hard disk image on your desktop using QEMU  
This will be faster than doing it on your android device.  
Once you are done you can copy the qcow2 image to your phone.  
  
Create a qcow2 image on your PC:  
qemu-img -f qcow2 slitaz.qcow2 10G  
  
Run the live linux distro in qemu and attach the Sliiso  
qemu-system-x86_64 -hda slitaz.qcow2 -cdrom slitaz.iso -net nic -m 512  
  
Install Slitaz to hard disk  
Click on Slitaz install and follow the steps  
When done remove the iso and boot with the hard disk only  
qemu-system-x86_64 -hda slitaz.qcow2 -net nic -m 512  

### Customization
Mouse acceleration under VNC  
From the options set mouse to 1.0 using the slider  
 
Resolution  
Change resolution to 800x600  
 click apply then save  
  
FTP Server  
Install ftp server if you want to access the VM filesystem from your android device:
tazpkg get-install pure-ftpd
to Start:
/etc/init.d/pure-ftpd start

SSH Server
To start the SSH server and connect from your Android device:
/etc/init.d/ssh start

To start FTP and SSH server automatically on boot:
edit /etc/rcS.conf and add to RUN_DAEMONS
RUN_DAEMONS="firewall httpd dropbear pure-ftpd"

### Notes:
Package Manager   
tazpkg -gi <package>  
  
update list:  
tazpkg recharge  
  
upgrade packages:  
tazpkg up  

If you see this message during boot time ignore it:  
Failed  to access perfctr msr  
Fast TSC Calibration Failed  
  
### Limbo Configuration with Hard Disk
cpu: x86  
memory: 512  
net: user  
nic: default  
hda: slitaz.qcow2  
  
Notes:  
To connect from android with SSH and FTP (Optional) use:  
hostfwd: tcp:22222:22,tcp:22221:21  
