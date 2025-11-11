## ANSWER


# 1. Create main directory and files
```
mkdir -p ~/file_mgmt
cd ~/file_mgmt
touch alpha.txt beta.txt gamma.txt
```

# 2. Create backup directory
``` 
mkdir -p ~/file_mgmt/backup
```

# 3. Copy alpha.txt into backup
```
cp alpha.txt ~/file_mgmt/backup/
```

# 4. Move beta.txt into backup
```
mv beta.txt ~/file_mgmt/backup/
```

# 5. Delete gamma.txt
```
rm -f gamma.txt
```

# 6. Verify results
```
ls -l ~/file_mgmt/backup
ls -l ~/file_mgmt
```

**Expected Output Example:**
```
# Inside ~/file_mgmt/backup
alpha.txt
beta.txt

# Inside ~/file_mgmt
backup/
```

---

### Notes
- `cp` copies files; `mv` moves them. 
- `rm -f` deletes files without prompting. 
- Always verify file actions using `ls -l`. 
