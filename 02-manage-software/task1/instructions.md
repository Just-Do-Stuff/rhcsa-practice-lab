# Category 02: Manage Software

This category focuses on managing RPM and Flatpak software repositories and packages on Red Hat-based systems.

---

## Task 1

**Exam Objectives:** 
- Configure access to RPM repositories 
- Install and remove RPM software packages 

---

## INSTRUCTIONS

1. Create a local directory `~/localrepo` to simulate a custom repository. 
2. Copy any `.rpm` package file (for example, from `/run/media` or `/usr/share`) into this directory. If none are available, use the `dnf download` command to get one. 
3. Create a local repository metadata structure using `createrepo`. 
4. Configure a new repository file under `/etc/yum.repos.d/localrepo.repo` that points to your local directory. 
5. Use `dnf` to verify the new repository is active. 
6. Install a package from that repository (for example, `tree`). 
7. Verify the package installation. 
8. Remove the installed package and verify it was removed. 

