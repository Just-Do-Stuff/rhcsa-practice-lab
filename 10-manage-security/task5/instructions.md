Task 5 — SELinux File Contexts for a Working Web Page (httpd + semanage)

## Purpose

This task simulates a realistic SELinux troubleshooting scenario:

- You install a web server.
- You place web content in a non-default directory.
- The web server cannot access the content due to incorrect SELinux file context.
- You must use `semanage` + `restorecon` to fix it.

---

## Scenario

You will configure Apache (`httpd`) to serve a simple web page from `/web` instead of the default `/var/www/html`.

Initially, the web page will not load due to incorrect SELinux file contexts, even though:
- File permissions are correct
- The firewall allows HTTP traffic

---

## Expected Result

- **Before SELinux fix:** accessing the site fails (commonly `403 Forbidden`)
- **After SELinux fix:** accessing the site returns your HTML page

---

## Instructions

1. Install the Apache web server and required SELinux management tools.
2. Create a new web root directory at `/web`.
3. Create an `index.html` file using elevated privileges.
4. Reconfigure Apache to use `/web` as its `DocumentRoot`.
5. Start and enable the web service.
6. Allow HTTP traffic through the firewall.
7. Test access to the web page (it should fail due to SELinux).
8. Identify the incorrect SELinux file context.
9. Use `semanage` to define the correct file context.
10. Apply the context with `restorecon`.
11. Verify the web page loads successfully.
