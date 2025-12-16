## Answer

```
systemctl status firewalld
systemctl start firewalld
systemctl enable firewalld

firewall-cmd --add-service=ssh --permanent
firewall-cmd --add-port=8080/tcp --permanent
firewall-cmd --reload
firewall-cmd --list-all
```
