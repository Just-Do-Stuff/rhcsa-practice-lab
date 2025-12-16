## Answer

# Verify current SELinux Mode
```
getenforce
```

# Set permissive mode
```
setenforce 0
```

# Verify current mode
```
getenforce
```

# Set enforcing mode
```
setenforce 1
```
