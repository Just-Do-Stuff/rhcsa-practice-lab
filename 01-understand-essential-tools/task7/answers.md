## ANSWER


# 1. Create the directory
```
mkdir -p ~/text_practice
```
# 2. Create and write the first line
```
echo "Welcome to the RHCSA practice lab" > ~/text_practice/welcome.txt
```

# 3. Append the second line
```
echo "You are learning essential Linux tools." >> ~/text_practice/welcome.txt
```

# 4. Verify contents
```
cat ~/text_practice/welcome.txt
```

**Expected Output Example:**
```
Welcome to the RHCSA practice lab
```

---

### Notes
- `>` overwrites files, while `>>` appends content. 
- `cat` displays file content quickly, useful for verification. 
- On the exam, you may also use `vi`, `vim`, or `nano` to edit files. 
