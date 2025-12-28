# autofs Practice 
=========================================

## Purpose

This section focuses on practicing autofs in the context of NFS, using two guided video walkthroughs. 
Setting up your own NFS server in a lab is extremely helpful for understanding how autofs behaves end‑to‑end.

This README points you to the videos to follow and clarifies what you should pay attention to for exam practice.

---

## Important Exam Note

> On the RHCSA exam you are expected to configure the client side (NFS mounts and possibly autofs), not build the NFS server from scratch.

In this lab:

- Configuring the NFS server is for practice only, so you can see the full flow. 
- Focus on understanding how:
  - NFS exports are presented from the server 
  - The client discovers and mounts those exports 
  - autofs automatically mounts and unmounts paths on demand

---
## Recommended Setup

For the best experience with these videos and autofs practice, use two VMs:

- VM1 – NFS Server
- VM2 – NFS Client (where you configure autofs)

Make sure that:

- Both VMs can reach each other over the network (ping by IP or hostname). 
- Basic name resolution works (either via `/etc/hosts` or DNS). 

---

## Videos to Watch

### 1. NFS Server Configuration (Practice Only)

This video walks through setting up an NFS server and exports:

▶ **NFS Server Setup:** 
<https://www.youtube.com/watch?v=wnzttj5AS30>

**What to focus on:**

- How the export directory is created (ownership and permissions). 
- How `/etc/exports` is configured. 
- How the NFS service is started and enabled. 
- How the client is allowed access (IP/network restrictions). 

Remember: **On the exam, the server side is usually setup for you.** 
You are practicing it here just so you understand what’s happening behind the scenes.

---

### 2. autofs Configuration on the Client (Exam‑Relevant)

This video walks through configuring autofs on the client to mount NFS exports automatically:

▶ **autofs Client Setup:** 
<https://www.youtube.com/watch?v=QmMVv4vI_5s>

**What to focus on:**

- Installing `autofs` if it is not already present. 
- How `/etc/auto.master` or `/etc/auto.master.d/*.autofs` is used. 
- How the map file is configured. 
- How the NFS server and export path are referenced in the map entry. 
- How to trigger the mount by accessing the directory. 
- Verifying that autofs mounts and unmounts automatically.



---

## How to Use This Section with the Repo

1. Watch Video 1 and optionally build a small NFS server on your server VM. 
2. Watch Video 2 and configure autofs on your client VM to mount the export from the server. 
3. After following the videos once, repeat the autofs setup from memory(highly recommend taking snapshots of your VMs so you can easily rollback:
   - Stop and disable autofs. 
   - Remove or rename your map file. 
   - Recreate the configuration without looking at notes if possible. 

Aim to repeat the full client‑side autofs configuration at least 20 times, just like the other tasks in this repo, until it feels natural and you can do it quickly under time pressure.

Practicing with your own NFS server in the lab simply gives you deeper understanding so the client‑side configuration feels straightforward on exam day.
