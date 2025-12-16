## Answer


# Check current umask
```
umask
```

# Set new umask
```
umask 027
```

# Verify by creating a file
```
touch testfile
ls -l testfile
```
