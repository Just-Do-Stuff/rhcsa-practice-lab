Category 02 — Manage Software
---

## Purpose

This category covers basic software management on Red Hat Enterprise Linux. 
The focus is on configuring software sources correctly and activating changes so you can install and remove packages as required on the RHCSA exam.

You will work with both RPM/DNF and Flatpak to simulate real-world package management tasks.

---

## Tools Used

For ease and consistency, all software management tasks in this category use:

- `dnf` – high-level package manager for managing RPM packages 
- `rpm` – low-level tool to query and verify installed RPMs 
- `flatpak` – framework for sandboxed desktop applications 
- Repository configuration files in `/etc/yum.repos.d/` 


---

## What You Will Practice

In this category, you will learn how to:

- Configure access to RPM repositories (including local `file://` repos). 
- Install and remove RPM software packages using `dnf`. 
- Configure access to Flatpak repositories (for example, Flathub). 
- Install and remove Flatpak software applications. 

Each practice task is split into **instructions** and **answers** so you can test yourself in an exam‑style workflow.

---

## Tasks and Layout in This Repo

### Task 1 – RPM Repositories and RPM Packages

You will:

- Create or configure access to an RPM/DNF repository. 
- Verify that the repository is active using `dnf repolist`. 
- Install an RPM package (for example, `tree`) from the configured repo. 
- Confirm installation with `rpm -q`. 
- Remove the package and verify it was removed.


---

### Task 2 – Flatpak Repositories and Applications

You will:

- Enable Flatpak support (if not already installed).  
- Add a Flatpak remote (such as Flathub).  
- Search for an application by ID (for example, `org.gnome.Calculator`).  
- Install a Flatpak application and verify it appears in `flatpak list`.  
- Optionally run the app to confirm it works.  
- Uninstall the application and verify it is removed.
