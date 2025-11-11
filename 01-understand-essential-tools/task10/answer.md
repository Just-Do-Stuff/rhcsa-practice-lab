NSWER 


# 1. Create directory and file
````
mkdir -p ~/permissions_practice
touch ~/permissions_practice/access.txt
```

# 2. Check current permissions
```
ls -l ~/permissions_practice/access.txt
```

# 3. Change permissions: owner=rw, group=r, others=none
```
chmod 640 ~/permissions_practice/access.txt
```

# 4. Verify permission change
```
ls -l ~/permissions_practice/access.txt
```

# 5. (Optional) Change file ownership to another user (replace 'practiceuser' if needed)
```
sudo chown practiceuser ~/permissions_practice/access.txt
```
# 6. Verify ownership and permissions again
```
ls -l ~/permissions_practice/access.txt
```

**Expected Output Example:**
```
-rw-r----- 1 practiceuser usergroup 0 Nov 10 10:15 access.txt
```

---

### Notes
- Use `chmod` in symbolic form (e.g., `chmod u=rw,g=r,o=`) or numeric (e.g., `chmod 640 file`).  
- `chown` changes file ownership — requires root privileges.  
- Always confirm results with `ls -l`.  
