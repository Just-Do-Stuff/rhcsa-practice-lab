## Task 4 - Access Remote Systems Using SSH

**Exam Category:** Understand and Use Essential Tools 

**Exam Objective:** Access remote systems using SSH 

---

**Purpose:** 
To practice connecting securely to remote systems using SSH, transferring files, and verifying success. 
If you don’t have a real remote system, you can still simulate this locally. Instructions are [here](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/blob/main/01-understand-essential-tools/task4/localhost_sim.md)

---

### Instructions (With Real Remote System)

1. Use SSH to connect to the remote system. 
2. Once connected, run the `hostname` command to confirm you’re on the remote host(this name will be different then you main host)
3. Exit the SSH session.
4. Create a local directory `remote_transfer`.
5. Use `scp` to copy `/etc/hosts` from your local system to the remote system’s `/tmp` directory.
6. Reconnect to the remote system and verify the file transfer to `/tmp`

