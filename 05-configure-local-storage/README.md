Category 05 & 06 — Local Storage Lifecycle (LVM, Filesystems, Swap)

## Purpose

Combining both catergories allows you to see the entire lifecycle of local storage.

- **Category 05** focuses on creating and persisting storage.
- **Category 06** focuses on resizing and removing that same storage.

All tasks are designed to build on top of each other.

---

## Before You Begin: Add a Virtual Disk for Storage Tasks

Most RHCSA storage tasks require a second disk. 
If you are practicing on a virtual machine, you **must add an additional virtual disk** before starting Category 05.

You may add a third disk if your environment allows.

---

## 1. Add a New Virtual Disk

### VMware / VirtualBox / Hyper-V / Proxmox / KVM

1. Shut down the VM (if required by your hypervisor).
2. Edit VM settings → **Add Hard Disk**.
3. Choose **SCSI** or **VirtIO** (recommended).
4. Disk size: 1-5 GB is enough for practice.
5. Start the VM.

---

## 2. Identify the Newly Added Disk

After booting, identify the new disk:

```bash
lsblk
sudo fdisk -l
```

Look for a disk with no existing partitions, commonly one of:

- `/dev/vdb`
- `/dev/sdb`
- `/dev/vdc`
- `/dev/sdc`

This disk will be referred to throughout Category 05 and 06 as your practice disk.

---

## 3. VERY IMPORTANT WARNINGS

- **NEVER modify `/dev/sda` or `/dev/vda`**
  - This is typically your OS disk
- Only use the disk you verified is empty
- All tasks in Category 05 and Category 06 will use the placeholder:

```
/dev/your_disk
```

Replace this placeholder with your actual practice disk (for example: `/dev/sdb`).

---

## Storage Lifecycle Flow (Read This First)

These categories are intentionally structured:

### Category 05 — Build Phase
You will:
- Partition disks
- Create PVs, VGs, and LVs
- Create filesystems
- Mount storage persistently using UUID or LABEL
- Create and persist swap

### Category 06 — Lifecycle Phase
You will:
- Extend logical volumes and filesystems
- Shrink logical volumes 
- Remove logical volumes safely

**Decisions made in Category 05 directly affect what is possible in Category 06.**

---

## Filesystem Rules (RHCSA Critical Knowledge)

| Filesystem | Can Extend | Can Shrink |
|-----------|----------|------------|
| **ext4**  | Yes | Yes (offline only) |
| **xfs**   | Yes | ❌ No |

If a task requires shrinking, the filesystem must be ext4. 
REMINDER: xfs cannot be shrunk. The only option is recreation.

---

## Notes

- Each task directory contains:
  - `instructions.md`
  - `answer.md` →
- Always verify your work using:
  - `lsblk`
  - `df -h`
  - `mount`
  - `swapon --show`

- These tasks are intentionally **destructive**...practice only on disposable disks.
- Category 05 builds storage correctly and persistently.
- Category 06 modifies or removes what was built.
- Filesystem choice in Category 05 directly impacts Category 06 options.
- Always verify mounts and swap after changes.

