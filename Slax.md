Slax: For those who want a currently active light weight linux distribution with a 5.x linux kernel and have a high end Android device.

You can download the live ISO from the official website:
https://www.slax.org

You can boot the live ISO from Limbo
## Limbo Configuration
cpu: x86  
memory: 512  
net: user  
nic: default  
cdrom: slax.iso

## Slax installation to hard disk (Optional)
Install Slax on the hard disk image on your desktop using QEMU.  
This will be faster than doing it on your android device.  
Once you are done you can copy the qcow2 image to your phone.  

### Virtual Hard Disk
Create a qcow2 image on your PC:  
qemu-img -f qcow2 slax.qcow2 10G  

### Boot from ISO:
Run the live linux distro in qemu and attach the Slax iso  
qemu-system-x86_64 -hda slax.qcow2 -cdrom slax.iso -net nic -m 512  

### Install qparted
apt-get install qparted  
 create an msdos partition table with qparted  
 create a partition ext2  
 format with ext3  
install bash if you don't have it  
apt-get install bash  
  
copy /slax folder from image to the new partition   
and run from within the hard disk:  
/boot/instboot.sh  
  
The detailed guide can be found here:  
https://www.slax.org/starting.php  
  
### Customization
hutdown the vm and remove the cdrom option and attach only the new hard driver:  
qemu-system-x86_64 -hda slax.qcow2 -net nic -m 512  
  
create a new user  
useradd -m tux --uid 1002 -U  
  
Install ftp server:  
apt-get install proftpd  
uncomment in the proftpd.conf:  
RequireValidShell       no  
/etc/init.d/proftpd start  
  
Notes  
to search in apt for a package:  
apt-cache search keyword  
  
### Limbo setup with hard disk  
cpu: x86  
memory: 512  
net: user  
nic: default  
hda: slax.qcow2  
  
Notes:  
To connect from android with SSH and FTP (Optional) use:  
hostfwd: tcp:22222:22,tcp:22221:21  