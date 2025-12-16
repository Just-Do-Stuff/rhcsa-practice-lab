Answer

```
umount /mnt/data
e2fsck -f /dev/vg_data/lv_data
resize2fs /dev/vg_data/lv_data 1G
lvreduce -L 1G /dev/vg_data/lv_data
mount /mnt/data
```

## Verify
```
df -h /mnt/data
```

> Shrinking cannot be done on xfs filesystems.
