Category 06 — Create and Configure File Systems
=================================================

## Purpose

This category focuses on using the storage you createdi in [Category 05](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/05-configure-local-storage). 
Here you will practice creating and mounting file systems, extending logical volumes, working with NFS, and using autofs for on‑demand mounts.

---

## Prerequisite: Read Category 05 First

> If you have **not** completed Category 05 — Configure Local Storage and read its [README.md](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/blob/main/05-configure-local-storage/README.md), go back and do that first.

Category 06 assumes you already know how to:

- Add an extra disk to your VM 
- Create partitions with `fdisk` 
- Build volume groups (VGs) and logical volumes (LVs)

In many of the tasks here, you will be reusing VGs and LVs that were created in Category 05. 
If those are missing, the examples in this category will not make sense.

---

## What You Will Practice in Category 06

In this category you will focus on:

- Creating and using ext4 and XFS file systems on existing LVs.
- Mounting and unmounting file systems at custom mount points.
- Extending logical volumes and growing their file systems.
- Practicing NFS client mounts.
- Configuring autofs so NFS shares are mounted automatically.


---

## autofs and NFS in This Category

In this repo:

- The `autofs/README.md` file points you to two short videos: 
  - One to help you practice configuring a simple NFS server (lab practice only). 
  - One to practice configuring autofs on the client, which is the exam-relevant part. 
- Setting up your own NFS server in a lab is optional but highly recommended, because it helps you see the entire flow.


Just like the other tasks in this repo, try to repeat the autofs setup(client side) many times until it feels natural and you can do it quickly without notes.

---



## Notes

- Category 05 builds storage correctly and persistently.
- Category 06 modifies or removes what was built, in addition to configuring autofs.
- Filesystem choice in Category 05 directly impacts Category 06 options.
- Always verify mounts and swap after changes.
