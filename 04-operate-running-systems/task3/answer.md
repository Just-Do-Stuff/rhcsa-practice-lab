## Answer


# 1. View logs
```
journalctl
```

# 2. Filter logs for a service
```
journalctl -u sshd
```

# 3. Logs since last boot
```
journalctl -b
```

# 4. Preserve journals permanently
```
sudo mkdir -p /var/log/journal
sudo systemd-tmpfiles --create --prefix /var/log/journal
```

# 5. Manage a network service
```
sudo systemctl start httpd
sudo systemctl stop httpd
sudo systemctl enable httpd
sudo systemctl status httpd
```

# 6. Copy file to remote system
```
scp file.txt user@x.x.x.x:/tmp/
```

# 7. Copy file from remote system
```
scp user@x.x.x.x:/etc/hosts ~/
```
