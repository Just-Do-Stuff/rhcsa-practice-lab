**Exam Category:** Understand and Use Essential Tools 
**Exam Objective:** Access remote systems using SSH 

---

## Task 4 — Access Remote Systems Using SSH

**Purpose:** 
To practice connecting securely to remote systems using SSH, transferring files, and verifying success. 
If you don’t have a real remote system, you can still simulate this locally. I will provide instructions

---

### Instructions (With Real Remote System)

1. Assume your remote system’s IP is `192.168.10.10` and the username is `admin`
2. Use SSH to connect to the remote system. 
3. Once connected, run the `hostname` command to confirm you’re on the remote host(this name will be different then you main host)
4. Exit the SSH session.
5. Create a local directory `remote_transfer`.
6. Use `scp` to copy `/etc/hosts` from your local system to the remote system’s `/tmp` directory.
7. Reconnect to the remote system and verify the file transfer to `/tmp`


### Insturctions If No Remote System

If you don’t have a second machine or virtual system to connect to, you can simulate SSH using **localhost** or by installing the SSH server locally.


### Install OpenSSH server (if not already installed)
```
sudo dnf install -y openssh-server
```

### Enable and start the SSH service
```
sudo systemctl enable --now sshd
```

### Verify it's running
```
sudo systemctl status sshd
```

### Simulate Connection and File Transfer
You can now use your **own machine’s hostname or IP** to practice SSH commands:

### Find your local IP address
```
hostname -I
```

### Connect to yourself using SSH
```
ssh YOURUSERNAME@localhost
```
### or
```
ssh YOURUSERNAME@127.0.0.1
```

### Verify connection
```
hostname
```
exit
