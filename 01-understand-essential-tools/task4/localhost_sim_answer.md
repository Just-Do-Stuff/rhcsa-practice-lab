## ANSWER (COMMANDS + VERIFICATION)

Use these commands directly to complete the localhost SSH simulation from start to finish.


# 1. Install and start SSH service
```
sudo dnf install -y openssh-server
sudo systemctl enable --now sshd
```

# 2. Verify SSH service is running
```
sudo systemctl status sshd
```
# 3. Get your local IP and hostname
```
hostname -I
hostname
```
# 4. Connect to yourself using SSH
```ssh USERNAME@localhost
```

# 5. Verify the connection (should display hostname)
```
hostname
```

# 6. Exit the SSH session
```
exit
```

# 7. Create a directory for file transfer
```
mkdir -p ~/remote_transfer
```

# 8. Copy /etc/hosts file to /tmp via scp
```
scp /etc/hosts USERNAME@localhost:/tmp/
```

# 9. Reconnect and verify that the file exists
```
ssh USERNAME@localhost "ls -l /tmp/hosts"

```

**Expected Output Example:**
```
-rw-r--r--. 1 USERNAME USERNAME 234 Nov  3 18:42 /tmp/hosts
```

---

## 🧾 Notes
- This method fully simulates SSH and SCP behavior even without a second system.  
- Always verify your work with `hostname` and `ls -l`. 
