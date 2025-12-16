Answer

```
umount /mnt/data
lvremove /dev/vg_data/lv_data
```

## Then edit /etc/fstab and remove entry


## Verify
```
lsblk
```
