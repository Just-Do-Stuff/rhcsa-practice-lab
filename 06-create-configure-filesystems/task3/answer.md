Answer

```
lvextend -L +500M /dev/vg_data/lv_data
resize2fs /dev/vg_data/lv_data
```

## Verify
```
df -h /mnt/data
```
