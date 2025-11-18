## ANSWER (COMMANDS + VERIFICATION)


# 1. Create local repository directory
mkdir -p ~/localrepo

# 2. Download an RPM package to simulate repo content (example: tree)
sudo dnf install -y dnf-plugins-core
sudo dnf download --destdir=~/localrepo tree

# 3. Install createrepo if not installed
sudo dnf install -y createrepo

# 4. Initialize the repository metadata
createrepo ~/localrepo

# 5. Create a repository configuration file
vim /etc/yum.repos.d/localrepo.repo 

```
[localrepo]
name=Local Repository
baseurl=file:///home/$USER/localrepo
enabled=1
gpgcheck=0
```

# 6. Verify repository is active
sudo dnf repolist

# 7. Install a package (example: tree) from the local repo
sudo dnf install -y tree

# 8. Verify installation
rpm -q tree

# 9. Remove the package
sudo dnf remove -y tree

# 10. Verify removal
rpm -q tree
```

---
