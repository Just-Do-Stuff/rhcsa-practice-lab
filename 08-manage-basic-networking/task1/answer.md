## Answer


# Launch NetworkManager TUI
```
nmtui
```

# Edit connection → IPv4 Configuration → Manual
# Enter Address / Prefix / Gateway appropriate for your subnet
# Activate the connection


# (Option A) Set hostname using nmtui
```
nmtui → Set system hostname
```

# (Option B) Set hostname using CLI
```
hostnamectl set-hostname server01.example.local
```

# Configure local hostname resolution
```
vim /etc/hosts
```

# Example entry (adjust IP to match your system):
```
192.168.1.50 server01.example.local server01
```
# Verify IP and hostname
```
ip addr
ip route
hostname
getent hosts
```
