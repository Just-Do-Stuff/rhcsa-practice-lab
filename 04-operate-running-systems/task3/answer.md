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
```
# 5. Open /etc/systemd/journald.conf. Find the Journal section
```
Storage=persistent
```

# 6. Restart Journal service
```
systemctl restart systemd-journald
```

# Verify
```
journalctl --disk-usage
ls -R /var/log/journal
```

# 7. Manage a network service
```
sudo systemctl start httpd
sudo systemctl stop httpd
sudo systemctl enable httpd
sudo systemctl status httpd
```

# 8. Copy file to remote system
```
scp file.txt user@x.x.x.x:/tmp/
```

# 9. Copy file from remote system
```
scp user@x.x.x.x:/etc/hosts ~/
```
