## Answer


# Create group
```
groupadd developers
```

# Add user to group
```
usermod -aG developers user1
```

# Verify membership
```
id user1
getent group developers
```
# Remove user from group
```
gpasswd -d user1 developers
```

# Delete group
```
groupdel developers
```
