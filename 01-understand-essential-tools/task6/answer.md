## ANSWER 


# 1. Create practice directory and files
```
mkdir -p ~/archive_practice
cd ~/archive_practice
echo "File 1 content" > file1.txt
echo "File 2 content" > file2.txt
echo "File 3 content" > file3.txt
```

# 2. Create a tar archive
```
tar -cvf ~/practice.tar ~/archive_practice
```

# 3. Compress using gzip
```
gzip ~/practice.tar
```

# 4. Verify compressed file exists
```
ls -l ~/practice.tar.gz
```

# 5. Decompress the gzip file
```
gunzip ~/practice.tar.gz
```

# 6. Compress again using bzip2
```
bzip2 ~/practice.tar
```

# 7. Verify .bz2 file exists
```
ls -l ~/practice.tar.bz2
```

# 8. Extract contents to new directory
```
mkdir -p ~/extracted
tar -xvf ~/practice.tar.bz2 -C ~/extracted --use-compress-program=pbzip2 || tar -xvf ~/practice.tar.bz2 -C ~/extracted --use-compress-program=bzip2
```

# 9. Verify extraction
```
ls -R ~/extracted
```

**Expected Output Example:**
```
file1.txt
file2.txt
file3.txt
```

---

### Notes
- Use `tar -cvf` to create archives, `tar -xvf` to extract. 
- Always verify compressed or extracted files with `ls -l` or `ls -R`. 
