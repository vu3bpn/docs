## To recover grub after install windows
### boot using any linux
### mount linux partition to /mnt
### mount /dev /dev/proc /proc /sys
### chroot to /mnt
### update-grub
### grub-install

* >sudo mount /dev/sdb3 /mnt
* >for i in /dev /dev/pts /proc /sys; do sudo mount -B $i /mnt$i; done
* >sudo chroot /mnt 
* >update-grub
* >grub-install /dev/sdb
