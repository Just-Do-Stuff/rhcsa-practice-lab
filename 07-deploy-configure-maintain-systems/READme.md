Category 07 — Deploy, Configure, and Maintain Systems

## Purpose

This category covers core system administration tasks aligned with **RHCSA exam objectives**.
All tasks assume a functioning Linux system with standard tools available.

The focus is on **using** system services and tools — not troubleshooting subscriptions or external dependencies.

---

## Repository Assumptions (IMPORTANT)

A valid software repository is **already configured** on the system by default.

This mirrors the RHCSA exam environment, where package repositories are provided and ready for use.

- No Red Hat subscription configuration is required
- Tasks focus on correct use of `dnf`

Even Rocky Linux default repositories are sufficient for practice.

---

## What You Will Practice

You will learn how to:

- Manage system services and enable them at boot
- Configure the system to boot into a specific target
- Schedule tasks using:
  - cron
  - at
  - systemd timer units
- Configure a time synchronization client
- Install and update software using the package manager
- Modify the system bootloader safely

---

## Safety Notice

Some tasks in this category modify critical system behavior (boot targets, bootloader).
You are strongly encouraged to:

- Practice on a virtual machine
- Take a snapshot before starting
- Avoid production systems

---

## Task Structure

Each task directory contains:

- `instructions.md` — exam-style task prompt
- `answer.md` — one valid solution

Multiple solutions may exist. Focus on meeting the objective.
