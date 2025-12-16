Task 3 — Configure SSH Key-Based Authentication

## Purpose

This task configures SSH key-based authentication, allowing a user to log in securely without a password.

Key-based authentication:
- Improves security over passwords
- Is commonly used for administration and automation
- Eliminates password prompts after setup

---

## Environment Requirement

To properly test SSH key-based authentication, you need:

- A client system (where the SSH key is generated)
- A server system (where the key is installed)

These may be:
- Two virtual machines on the same subnet
- One virtual machine and another reachable Linux system

---

## Instructions

1. Log in as a non-root user on the client system.
2. Generate an SSH key pair for the user.
3. Copy the public key to the server system.
4. Log in to the server using SSH.
5. Verify that no password prompt appears.

---

## Expected Result

- SSH login succeeds without requesting a password
- Authentication uses the SSH key
