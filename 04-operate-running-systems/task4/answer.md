## Answer 
### 1. Interrupt the Boot Process at GRUB

1. Reboot the system:
```
sudo reboot
```

2. When the GRUB menu appears, highlight the default boot entry and press **`e`** to edit it.

3. Find the line that starts with `linux` (or `linux16` / `linuxefi` depending on the system).  
At the end of that line, append:
```
init=/bin/bash
```

4. Press **`Ctrl + X`** to boot with the modified parameters.
The system will boot into a root shell without prompting for a password


### 2. Remount Root Filesystem as Read-Write

By default, the root filesystem is mounted read-only in this mode. 
Remount it read-write:

```
mount -o remount,rw /
```

You can verify with:

```
mount | grep ' / '
```

---

### 3. Reset the Root Password

Run:

```
passwd root
```

Enter the new password as required by the task. 
Confirm the password when prompted.

---

### 4. Prepare for SELinux Relabeling

To ensure SELinux contexts are corrected on the next boot, create the autorelabel flag file:

```
touch /.autorelabel
```

This tells the system to relabel files on the next full boot if SELinux is enforcing or permissive.

---

### 5. Continue the Boot Process Normally

Instead of rebooting abruptly, start systemd cleanly from this shell:

```
exec /usr/lib/systemd/systemd
```

The system will continue booting into its normal target. 
The SELinux relabel may take some time on the next boot, depending on disk size.

---

### 6. Verify Root Login with New Password

Once the system reaches the login prompt:

1. Log in as `root` with the new password you set
 

2. Confirm access by running:
```
whoami
```

You should see:
```
root
```
