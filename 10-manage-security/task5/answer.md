## Answer


# 1) Install Apache and SELinux utilities. This should already be available on exam.
```
dnf install -y httpd policycoreutils-python-utils
```
# 2) Create non-default web root
```
mkdir -p /web
```

# 3) Create index.html using elevated privileges (permission-safe method)
```
sudo tee /web/index.html <<EOF
<h1>SELinux fixed. It works!</h1>
EOF
```

# 4) Reconfigure Apache DocumentRoot
```
vim /etc/httpd/conf/httpd.conf
```
### Update the following:

DocumentRoot '/web'
  <Directory '/web'>
    AllowOverride None
     Require all granted
  </Directory>
 

# 5) Start and enable Apache
```
systemctl enable --now httpd
```

# 6) Allow HTTP through the firewall
```
systemctl enable --now firewalld
firewall-cmd --add-service=http --permanent
firewall-cmd --reload
```

# 7) Test access (expected to FAIL initially due to SELinux)
```
curl -I http://localhost
curl http://localhost
```
# Confirm SELinux is enforcing and check contexts
```
getenforce
ls -Zd /web /web/index.html
```

# (View Logs)
```
journalctl -t setroubleshoot --no-pager
```

# 8) Define correct SELinux context for the new web root
```
semanage fcontext -a -t httpd_sys_content_t "/web(/.*)?"
```
# 9) Apply context changes
```
restorecon -Rv /web
```

# Verify contexts
```
ls -Z /web /web/index.html
```

# 10) Test again (should now work)
```
curl http://localhost
```

---
Lets say we do everything right and the issue doesnt resolve. It could be the listening port is using the wrong port, so we need to correct it.

This section reinforces SELinux port labeling concepts.

### Scenario
You want Apache to listen on port **8080** instead of 80.

### Steps


# 1) Update Apache listen port
vim /etc/httpd/conf/httpd.conf
# Find Listen block in the file and change to 8080:
```
Listen 8080
```
# 2) Open firewall port
```
firewall-cmd --add-port=8080/tcp --permanent
firewall-cmd --reload
```

# 3) Label port for httpd in SELinux
```
semanage port -a -t http_port_t -p tcp 8080
```

# 4) Restart Apache
```
systemctl restart httpd
```

# 5) Test
```
curl http://localhost:8080
```

---

## Key Takeaways

- Filesystem permissions does not equal SELinux permissions.
- `semanage fcontext` defines what the context should be.
- `restorecon` applies the defined context.
- SELinux blocks access silently unless you inspect contexts or AVC logs.
- Port changes require **both** firewall and SELinux updates.
