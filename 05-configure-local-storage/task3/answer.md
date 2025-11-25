## Answer

### Swap via partition
```
sudo mkswap /dev/your_disk3
sudo swapon /dev/your_disk3
sudo swapon --show
sudo swapoff /dev/your_disk3
```

### Swap via LV
```
sudo lvcreate -L 256M -n lvswap labvg
sudo mkswap /dev/labvg/lvswap
sudo swapon /dev/labvg/lvswap
sudo swapon --show
sudo swapoff /dev/labvg/lvswap
```
