## Answer


# Add user to wheel group (recommended method)
```
usermod -aG wheel user1
```

# Verify sudo access
```
id user1
```

# Test (as user1 by logging in as that user)
```
sudo whoami
```

# Remove sudo access
```
gpasswd -d user1 wheel
```

# Verify removal
```
id user1
```
