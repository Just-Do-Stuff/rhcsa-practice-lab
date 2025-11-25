## Answer


# 1. Reboot system normally

```
sudo reboot
```
# 2. Shut down safely
```
sudo shutdown -h now
```

# 3. View current default target
```
systemctl get-default
```

# Change default target to multi-user
```
sudo systemctl set-default multi-user.target
```

# 4. Switch to graphical target immediately
```
sudo systemctl isolate graphical.target
```

# 5. Interrupt boot (manual GRUB step, not a command)

```
At GRUB menu: press 'e', append 'init=/bin/bash' to end of kernel line, then press CTRL + X
```

# 6. Reset root password 
```
mount -o remount,rw /
passwd root
touch /.autorelabel
exec /usr/lib/systemd/systemd
```

# 6.1 Additional way to reset password
```
mount -o remount,rw /sysroot
chroot /sysroot
passwd root
touch /.autorelabel
exit
```
