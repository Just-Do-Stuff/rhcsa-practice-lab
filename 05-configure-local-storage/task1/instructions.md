Task 1 — Create LVM Storage and Mount Persistently

### Instructions

1. Create a new partition using `fdisk` on a secondary disk for LVM usage.
2. Initialize the partition as a Physical Volume (PV).
3. Create a Volume Group named `vg_data`.
4. Create a Logical Volume named `lv_data` with a size of 2G.
5. Format the LV with an ext4 filesystem.
6. Assign a filesystem label.
7. Mount the filesystem at `/mnt/data`.
8. Configure the mount to persist across reboots using UUID or LABEL.
9. Verify the mount.
