ategory 05: Configure Local Storage (Main Tasks)

These tasks use **fdisk** and LVM. Replace `/dev/your_disk` with the disk you created via README[]

---

# Task 1 — Create a Partition, PV, VG, LV

## Instructions
1. Identify your practice disk (`lsblk`).
2. Create a 500M partition using `fdisk`.
3. Change partition type to Linux LVM.
4. Create a Physical Volume, Volume Group, and Logical Volume.
5. Remove the LV, VG, and PV safely.
