Category 08 — Manage Basic Networking

## Purpose

This category covers basic network configuration tasks.
The focus is on configuring networking using NetworkManager tools, making sure changes are activated and persistent.

---

## Core Exam Objectives Covered

You will practice how to:

- Configure IPv4 and IPv6 addresses
- Configure hostname resolution
- Ensure network services start automatically at boot
- Restrict network access using firewalld and firewall-cmd

---

## IMPORTANT: Activating Network Changes

⚠️ **This is critical for RHCSA success OR YOU WILL FAIL THE EXAM**

Making network changes does **NOT** automatically apply them.

After configuring a network connection, you **must activate it** for changes to take effect.

Failure to activate the connection is one of the most common causes of FAILING the exam.

---

## Tooling Choice: nmtui (Recommended for exam)

Why nmtui:
- Reduces syntax errors
- Ensures NetworkManager compatibility
- Ideal for exam environments

---

## Activation Rules (Read Carefully)

After making changes in nmtui, you must:

- Reactivate the connection
  - Either by disconnecting/reconnecting
  - Or by restarting NetworkManager

If the network is not activated:
- IP changes will not apply
- Hostname resolution tests may fail
- Firewall tests may appear broken

---

## Safety Notes

- Always confirm your active connection before modifying it
- Avoid disconnecting your only network interface on a remote system
- Practice on a local VM when possible

---

## Task Structure

Each task includes:

- `instructions.md` — exam-style task description
- `answer.md` — one valid solution

Multiple solutions may exist. Focus on achieving the required **outcome**.
