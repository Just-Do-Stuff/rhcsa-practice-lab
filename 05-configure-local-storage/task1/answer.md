Answer

# Create partition (fdisk)
```
fdisk /dev/your_disk
```
# Create PV, VG, LV
```
pvcreate /dev/your_disk
vgcreate vg_data /dev/your_disk
lvcreate -L 1G -n lv_data vg_data
```
# Create filesystem and label
```
mkfs.ext4 /dev/vg_data/lv_data
e2label /dev/vg_data/lv_data DATA_VOL
```
# Create mount point and mount
```
mkdir /mnt/data
mount /dev/vg_data/lv_data /mnt/data
```
# Get UUID
```
blkid /dev/vg_data/lv_data
```
# Add to /etc/fstab (example using LABEL)
```
LABEL=DATA_VOL /mnt/data ext4 defaults 0 0
```
# Verify
```
mount -a
df -h
```
