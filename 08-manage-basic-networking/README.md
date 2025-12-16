Category 08 — Manage Basic Networking

## Purpose

This category covers basic network configuration and security.
The focus is on configuring network settings correctly and activating changes.

---

## Tools Used

For ease and consistency, all network configuration tasks in this category use:

- **nmtui** (NetworkManager Text User Interface)

nmcli is another tool we can use but for the exam use nmtui to avoid syntax errors.

---

## VERY IMPORTANT: Network Activation

⚠️ **Network changes do NOT take effect until the connection is activated.**

After making changes in `nmtui`, you must:
- Activate the modified connection
- Or bring the connection down and back up

Failure to activate the connection is one of the most common reasons people **FAIL** the exam.

# ACTIVATE THE NETWORK, ACTIVATE THE NETWORK, ACTIVATE THE NETWORK!!!!!

---

## Network Addressing Requirement

Always configure static IP addresses within your local subnet.

Using an IP outside your network will result in loss of connectivity unless routing or VLANs are configured (out of scope topic. RHCSA will not be testing on that).

Before configuring a static IP, you should:

1. Identify your current network details
2. Verify:
   - IP address range
   - Subnet mask / prefix
   - Default gateway

Use the following commands to inspect your network:

```
ip addr
ip route
nmcli device status
```

Use this information to choose an appropriate static IP address for your environment.

---

## What You Will Practice

You will learn how to:

- Configure IPv4 and IPv6 addresses
- Configure hostname resolution
- Configure network services to start automatically at boot
- Restrict network access using `firewalld`

---

## Safety Notice

Network misconfiguration can cause **loss of connectivity**.

You are strongly encouraged to:
- Practice on a virtual machine
- Use console access (not SSH) while learning
- Take a snapshot before starting

