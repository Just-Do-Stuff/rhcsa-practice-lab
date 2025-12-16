## Answer


# List ports
```
semanage port -l | grep http
```
# Add port label
```
semanage port -a -t http_port_t -p tcp 8080
```
# List booleans
```
getsebool -a
```
# Enable boolean persistently
```
setsebool -P httpd_can_network_connect on
```
# Verify
```
getsebool httpd_can_network_connect
```
