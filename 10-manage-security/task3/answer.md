## Answer


# Generate SSH key pair (client)
```
ssh-keygen # For simple key creation


ssh-keygen -t rsa -b 4096 -C "your_comment_here" # A little more advanced way to create the key

```
# Copy public key to server
```
ssh-copy-id user@server_ip
```
# Test login
```
ssh user@server_ip
```

# Verify
```
hostname
whoami
```

