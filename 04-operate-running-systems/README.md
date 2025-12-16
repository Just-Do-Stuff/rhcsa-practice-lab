##Category 04 — Operate Running Systems

---

## Purpose

- This category focuses on operational control of a running Red Hat Enterprise Linux system. 
- The goal is to make you comfortable with keeping a system healthy, responsive, and recoverable under pressure.


---

## VERY IMPORTANT: Safe Reboots and Recovery

> Changes to targets, boot parameters, and services can lock you out if done incorrectly.

Before attempting recovery or boot‑related tasks, keep in mind:

- Always verify what target you are switching to with:
  ```
  systemctl get-default
  ```
- When changing the default target, confirm you can still log in after a reboot. 
- Always test critical changes while you still have a working session open (for example, a second terminal or console), so you are not locked out.

Failure to plan boot and service changes is a common reason candidates lose time—or temporarily lose access—on the exam.

---

## What You Will Practice

In this category, you will learn how to:

- Boot, reboot, and shut down a system.
- Change and isolate systemd targets (multi‑user, graphical).
- Interrupt the boot process using GRUB to reach recovery/emergency mode.
- Identify CPU and memory‑intensive processes and terminate them if necessary.
- Adjust process scheduling with `nice` and `renice` 
- Apply and verify tuning profiles with `tuned-adm` 
- View and filter logs using `journalctl` and `/var/log` 
- Start, stop, enable, and check the status of services.
- Securely transfer files between systems.

---

## How This Category Is Organized

Each task in this category is split into two files:

- `instructions.md` – the exam‑style prompt describing the situation and required outcome.
- `answer.md` – one possible solution with commands and example verification steps. 

**Recommended workflow:**

2. Read `instructions.md` and complete the task on your own. 
3. Open `answer.md` only after you have attempted the task or need help troubleshooting.

---

## Tasks in This Category

### Task 1 – Boot, Shutdown, and Targets

You will practice:

- Rebooting and shutting down the system normally.
- Checking and changing the default systemd target.
- Switching between multi‑user and graphical targets without rebooting.
- Interrupting the boot process at GRUB and using emergency mode for recovery (for example, root password reset).


---

### Task 2 – Process and Performance Management

You will practice:

- Listing the most CPU‑ and memory‑intensive processes.
- Killing misbehaving processes by PID.
- Starting a process with adjusted priority using `nice`
- Changing the priority of an existing process using `renice` 
- Listing available tuning profiles and applying a performance‑oriented profile with `tuned-adm`



---

### Task 3 – Logs, Journals, Services, and Secure File Transfer

You will practice:

- Viewing system logs with `journalctl` 
- Filtering logs for a specific service (for example, `sshd`) 
- Showing logs from the current boot only.
- Ensuring journals are preserved by configuring persistent storage.
- Starting, stopping, enabling, and checking the status of a network service with `systemctl`
- Using `scp` to securely transfer files to and from another system.



---

## How This Connects to the Exam

- Keep a system running and reachable 
- Recover gracefully from boot or service problems.
- Prove that you can read logs, interpret what’s happening, and take corrective action.
- Safely manage processes and apply tuning where needed.
- Use SSH and SCP as your basic remote access tools.

