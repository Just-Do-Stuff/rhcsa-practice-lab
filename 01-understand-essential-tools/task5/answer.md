## ANSWER 


# 1. Verify the system target (should show multi-user.target)
```
systemctl get-default
```

# 2. Switch to the root user
```
su -
```

# 3. Verify current user
```
whoami
```

# 4. Exit root shell
```
exit
```

# 5. Create a new user account
```
sudo useradd practiceuser
sudo passwd practiceuser
```

# 6. Switch to the new user
```
su - practiceuser
```

# 7. Confirm the new user identity
```
whoami
```

# 8. Return to your original user
```
exit
```

## Expected Output Example:
```
#1 multi-user.target
#3 root
#7 practiceuser
```

---

### Notes
- `su -` starts a full login shell for the target user. 
- Always verify your target runlevel or systemd target with `systemctl get-default`
- You can change to a different target using `sudo systemctl isolate multi-user.target`

