Answer

```
lvcreate -L 512M -n lv_swap vg_data
mkswap /dev/vg_data/lv_swap
swapon /dev/vg_data/lv_swap
```

# Persist swap
```
blkid /dev/vg_data/lv_swap
```

# Add to /etc/fstab
```
UUID=<swap-uuid> swap swap defaults 0 0
```

# Verify
```
swapon --show
```
