## Answer

```
grubby --update-kernel=ALL --args="quiet"
grub2-mkconfig -o /boot/grub2/grub.cfg
```
