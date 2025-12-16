## Answer

```
timedatectl
systemctl status chronyd
chronyc sources -v
```

## If the system is not synchronized. It will say
- System clock synchronized: no

```
systemctl restart chronyd
chronyc sources -v
timedatectl
```
