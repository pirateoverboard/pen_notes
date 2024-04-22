
`sudo df -h`

`sudo mount /dev/mapper/vda5_crypt /mnt`

`sudo btrfs subvolume create /mnt/@opt`

`sudo mv /opt/* /mnt/@opt`

`sudo umount /mnt`

`sudo nano /etc/fstab`

fine line with /home - CRTL-K then CRTL_U twice

`sudo systemctl daemon-reload`

`sudo mount -av`

