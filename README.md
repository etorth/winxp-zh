# winxp-zh
传奇3xp

Serials:

DG8FV-B9TKY-FRT9J-6CRCC-XPQ4G

6YDH3-GPKVM-2DX3V-WDXQM-BHWGJ

3KHMJ-DW7BX-77XHM-DFCW3-J4GHW


since you may not have permission to use public computer to create the usb booter, there is an easy way to do it:
from: https://forums.linuxmint.com/viewtopic.php?t=174570


With SteveSi's feedback, which is good news for simplifying the process.

Here is a revised short process :

1. Format the USB flash with FAT32.
   this is easy, use linux command or just insert usb to windows computer and format to FAT32

2. Make a directory e2b to store the easy2boot zip archive file.

3. Download the file Easy2Boot.zip from the link:
https://www.fosshub.com/Easy2Boot.html

keep in mind that you need to download the version with xp support.
If you are gooing to use Linux to make the booter, download the .zip version.

Save it into the above e2b directory, it's just a archive, needs to extrat to usb in step-6.
the extract passowrd is e2b

4. Cd to e2b directory, get into root terminal

5. Mount the USB flash with mount /dev/sdb1 /mnt

root@trios:/home/wayne/e2b# mount /dev/sdb1 /mnt

6. Extract the above file directly to root of the USB flash

root@trios:/home/wayne/e2b# unzip Easy2Boot_v1.53.zip -d /mnt

7. cd to the directory containing the bootlace file

root@trios:/# cd /mnt/_ISO/docs/linux_utils/

8. Install bootlace to USB flash

root@trios:/mnt/_ISO/docs/linux_utils# ./bootlace.com --time-out=0 /dev/sdb

9. Use the GUI File Manager ( or command lines) in linux,
copy livecd ISOs to the /_ISO/MAINMENU folder or /_ISO/LINUX folder

just an example, I use Linux command to copy iso files to /_ISO/LINUX folder

root@trios:/home/wayne/Downloads# cp debian-7.6.0-amd64-DVD-1.iso /mnt/_ISO/LINUX/
root@trios:/home/wayne/Downloads# cp systemrescuecd-x86-4.3.0.iso /mnt/_ISO/LINUX/
root@trios:/home/wayne/Downloads# cp debian-live-7.5.0-amd64-xfce-desktop+nonfree.iso /mnt/_ISO/LINUX/

For window xp, needs to copy to _ISO/WINDOWS/XP/<xp.iso>

#cp sparkylinux-3.4.1-x86_64-base.iso pmagic_2013_08_10_reconstructed.iso  Porteus-XFCE-v3.0-i486.iso Porteus-MATE-v3.0-i486.iso /mnt/_ISO/LINUX/

That is all.

Easier process than before, thanks to SteveSi's Easy2Boot...v1.53

with this, it is easy to make multiboot USB flash or USB drive too. :mrgreen:
