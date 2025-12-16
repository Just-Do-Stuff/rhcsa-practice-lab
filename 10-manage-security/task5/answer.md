## Answer


# 1) Install Apache + SELinux management utilities
```
dnf install -y httpd policycoreutils-python-utils
```
# 2) Create a non-default web root and a simple page
```
mkdir -p /web
echo '<h1>SELinux fixed — it works!</h1>' > /web/index.html
```
# 3) Reconfigure Apache to serve from /web
# Update DocumentRoot and the matching <Directory> block
```
vim /etc/httpd/conf/httpd.conf
```
# Make these two changes:
# DocumentRoot "/web"
# <Directory "/web">
#     AllowOverride None
#     Require all granted
# </Directory>

# 4) Start and enable httpd
```
systemctl enable --now httpd
```
# 5) Allow HTTP through the firewall (permanent)
```
systemctl enable --now firewalld
firewall-cmd --add-service=http --permanent
firewall-cmd --reload
```
# 6) Test locally (this often FAILS first due to SELinux contexts)
```
curl -I http://localhost
curl http://localhost
```

# If it fails, confirm SELinux is enforcing and inspect contexts
```
getenforce
ls -Zd /web /web/index.html
```
# (Optional but helpful) Look for SELinux denial messages
```
journalctl -t setroubleshoot --no-pager
```

# 7) Fix: define correct SELinux context for the new web root
# This tells SELinux that anything under /web is web content
```
semanage fcontext -a -t httpd_sys_content_t "/web(/.*)?"
```

# 8) Apply the context change to the filesystem
```
restorecon -Rv /web
```
# Verify contexts are now correct
```
ls -Z /web /web/index.html
```
# 9) Test again (should now work)
```
curl http://localhost
```
