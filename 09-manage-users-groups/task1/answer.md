## Answer


# Create user
```
useradd user1
passwd user1
```

# Modify user shell
```
usermod -s /bin/bash user1
```
# Verify
```
id user1
getent passwd user1
```
# Delete user and home directory
```
userdel -r user1
```
