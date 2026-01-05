sudo blkid /dev/mmcblk0p3
/dev/mmcblk0p3: LABEL="data" UUID="91c5b18b-7740-46e9-ad2e-e08bb09bb711" BLOCK_SIZE="4096" TYPE="ext4" PARTUUID="c6c21c02-03"

sudo mkdir -p /mnt/data_partition
sudo mount /dev/mmcblk0p3 /mnt/data_partition

sudo ls -la /mnt/data_partition/
total 28
drwxr-xr-x 4 root root  4096 Dec 17 03:12 .
drwxr-xr-x 3 root root  4096 Jan  5 05:39 ..
drwx------ 2 root root 16384 Dec 17 03:12 lost+found
drwxr-xr-x 3 root root  4096 Dec 17 03:12 overlay

sudo find /mnt/data_partition -type f 2>/dev/null
/mnt/data_partition/overlay/etc/systemd/system/systemd-remount-fs.service.d/overlayroot.conf

