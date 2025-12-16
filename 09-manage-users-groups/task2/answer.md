## Answer

# If user doesnt exist, create the user.

# Set or change password
```
passwd user2
```
# Configure password aging
```
chage -M 90 -W 7 user2
```

# Verify
```
chage -l user2
```
