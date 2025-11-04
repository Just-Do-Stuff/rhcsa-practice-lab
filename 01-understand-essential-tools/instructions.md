Task 4

**Exam Category:** Understand and Use Essential Tools 
**Exam Objective:** Access remote systems using SSH 

**Purpose:** 
To practice secure shell (SSH) connections between systems and transferring files securely.

### Instructions
1. Assume your remote system’s IP is `192.168.10.10` and the username is `admin`
2. Use SSH to connect to the remote system
3. Once connected, run the `hostname` command to confirm access
4. Exit the session 
5. Create a directory `remote_transfer`
6. Use `scp` to copy `/etc/hosts` from your local machine to the remote system’s `/tmp` directory
7. Re-connect to the remote system and **verify** that the file was successfully transferred to `/tmp`.  
