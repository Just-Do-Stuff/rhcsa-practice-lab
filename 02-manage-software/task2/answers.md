ANSWER (COMMANDS + VERIFICATION)


# 1. Install Flatpak if not available
```
sudo dnf install -y flatpak
```

# 2. Add the Flathub repository
```
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

# 3. Verify repository configuration
```
flatpak remotes
```

# 4. Search for a package (example: GNOME Calculator)
```
flatpak search org.gnome.Calculator
```

# 5. Install the package
```
sudo flatpak install -y flathub org.gnome.Calculator
```

# 6. Verify installation
```
flatpak list
```

# 7. (Optional) Run the application
```
flatpak run org.gnome.Calculator
```

# 8. Uninstall the package
```
sudo flatpak uninstall -y org.gnome.Calculator
```
# 9. Verify removal
```
flatpak list | grep Calculator || echo "Flatpak application successfully removed"
```

**Expected Output Example:**
```
Remotes:
Name     Options
flathub  system

Found similar ref(s) for ‘org.gnome.Calculator’
Installing: org.gnome.Calculator/x86_64/stable from flathub
Complete!
Flatpak application successfully removed
```

---

### Notes
- Flatpak apps are sandboxed and installed system-wide or per-user.  
- Use `flatpak list` and `flatpak remotes` to verify configuration.  
- RHCSA focuses on repository setup and command familiarity, not GUI interaction.  
