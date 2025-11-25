## Answer
```
lsblk

sudo fdisk /dev/your_disk
```
``` # The inputs
# n
# 1
# <enter>
# +500M
# t
# 31
# w

```
sudo pvcreate /dev/your_disk1
sudo vgcreate labvg /dev/your_disk1
sudo lvcreate -L 300M -n lablv labvg
sudo lvs
sudo vgs
sudo lvremove -y /dev/labvg/lablv
sudo vgremove -y labvg
sudo pvremove -y /dev/your_disk1
```
