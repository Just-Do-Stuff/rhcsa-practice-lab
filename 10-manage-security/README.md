# Category 10 — Manage Security

## Purpose

This category covers core system security tasks.
The focus is on host-based security controls.

---

## What You Will Practice

You will learn how to:

- Configure firewall rules using `firewalld`
- Manage default file permissions using `umask`
- Configure SSH key-based authentication
- Manage SELinux modes (enforcing vs permissive)
- Identify SELinux file and process contexts
- Restore default SELinux file contexts
- Manage SELinux port labels
- Modify SELinux behavior using booleans

---

## Environment Requirement 

Some tasks in this category require more than one system to fully understand what is going on.

In particular:
- SSH key-based authentication requires:
  - A client system (where the SSH key is generated)
  - A server system (where the key is used to log in)

This may be accomplished using:
- Two virtual machines on the same network, or
- One virtual machine and another reachable Linux system

If only one system is available, testing against `localhost` is acceptable but provides limited validation.

## Scope Notes

- These tasks focus on local system security.
- Advanced firewall topics (NAT, rich rules) are out of scope
- SELinux policy creation is out of scope.

---

## Quick Disclaimer

Security misconfiguration can result in:
- Loss of access (SSH/firewall)
- Application failures (SELinux)

You are strongly encouraged to:
- Practice on a virtual machine
- Use console access when modifying SELinux or firewall rules
- Verify every change
