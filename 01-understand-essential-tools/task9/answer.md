## ANSWER 


# 1. Create practice directory and file
```
mkdir -p ~/link_practice
echo "Link practice file" > ~/link_practice/original.txt
```

# 2. Create a hard link
```
ln ~/link_practice/original.txt ~/link_practice/hardlink.txt
```

# 3. Create a soft (symbolic) link
```
ln -s ~/link_practice/original.txt ~/link_practice/softlink.txt
```

# 4. Verify links
```
ls -l ~/link_practice
```

# 5. Modify the original file
```
echo "Updated content for link testing" >> ~/link_practice/original.txt
```

# 6. View all files to confirm synchronization
```
cat ~/link_practice/original.txt
cat ~/link_practice/hardlink.txt
cat ~/link_practice/softlink.txt
```

**Expected Output Example:**
```
Link practice file
Updated content for link testing
Link practice file
Updated content for link testing
Link practice file
Updated content for link testing
```

---

### Notes
- A **hard link** is a duplicate reference to the same inode — deleting the original doesn’t remove the data. 
- A **soft (symbolic) link** is a pointer — if the original f
