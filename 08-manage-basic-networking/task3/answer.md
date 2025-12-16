## Answer

# Verify and enable firewalld
```
systemctl status firewalld
systemctl start firewalld
systemctl enable firewalld
```
# Identify active zones
```
firewall-cmd --get-active-zones
```
# Allow a service (example: https)
```
firewall-cmd --add-service=https --permanent
```
# Allow a port (example: TCP 8080)
```
firewall-cmd --add-port=80/tcp --permanent
```
# Apply changes
```
firewall-cmd --reload
```
# Verify rules
```
firewall-cmd --list-all
```
