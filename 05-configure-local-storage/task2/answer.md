## Answer
```
sudo fdisk /dev/your_disk
```

## The inputs:  n, 2, +500M, t, 31, w

```
sudo pvcreate /dev/your_disk2
sudo vgextend labvg /dev/your_disk2
sudo lvcreate -L 200M -n newlv labvg
```
