# Before You Begin: Adding a Virtual Disk for Storage Tasks

Most RHCSA storage tasks require a second disk. If you are practicing on a VM, you must add a virtual hard disk in order to complete Category 05 & 06 tasks.

---

## 1. Add a New Virtual Disk 

### VMware / VirtualBox / Hyper‑V / Proxmox / KVM
1. Shut down the VM (if required by the hypervisor).
2. Edit VM settings → Add Hard Disk.
3. Choose SCSI or VirtIO (recommended).
4. Size: **1–5 GB** is enough for practice.
5. Start the VM.

---

## 2. Identify the Newly Added Disk

Run:

```bash
lsblk
sudo fdisk -l
```

Look for a disk with no partitions, usually one of:

- `/dev/vdb`
- `/dev/sdb`
- `/dev/vdc`
- `/dev/sdc`

This is your **practice disk**.

---

## 3. VERY IMPORTANT WARNINGS

- **NEVER touch `/dev/sda` or `/dev/vda`** – this is usually your OS disk.
- Only use the disk you identified as **empty**.
- All tasks in Category 05 & 06 will use the placeholder:

```
/dev/your_disk
```

Replace it with your actual practice disk.
