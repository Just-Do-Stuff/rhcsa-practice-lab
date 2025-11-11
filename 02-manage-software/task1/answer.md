## ANSWER (COMMANDS + VERIFICATION)


# 1. Create local repository directory
mkdir -p ~/localrepo

# 2. Download an RPM package to simulate repo content (example: tree)
sudo dnf install -y dnf-plugins-core
dnf download tree --destdir=~/localrepo

# 3. Install createrepo if not installed
sudo dnf install -y createrepo

# 4. Initialize the repository metadata
createrepo ~/localrepo

# 5. Create a repository configuration file
sudo tee /etc/yum.repos.d/localrepo.repo <<EOF
[localrepo]
name=Local Repository
baseurl=file:///home/$USER/localrepo
enabled=1
gpgcheck=0
EOF

# 6. Verify repository is active
sudo dnf repolist

# 7. Install a package (example: tree) from the local repo
sudo dnf install -y tree

# 8. Verify installation
rpm -q tree

# 9. Remove the package
sudo dnf remove -y tree

# 10. Verify removal
rpm -q tree || echo "Package successfully removed"
```

**Expected Output Example:**
```
Repo-id          Repo-name
localrepo        Local Repository
Installing: tree
Complete!
tree-1.8.0-10.el9.x86_64
Package successfully removed
```

---
