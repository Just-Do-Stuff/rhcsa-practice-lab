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

Initially, the page will not load because `/web` has the wrong SELinux context.

---

## Expected Result

- Before SELinux fix: accessing the site fails (commonly 403 Forbidden)
- After SELinux fix: accessing the site returns your HTML page

---

## Instructions

1. Install the Apache web server (`httpd`) and required SELinux tools.
2. Create a new web root directory at `/web` and add an `index.html` page.
3. Reconfigure Apache to use `/web` as its `DocumentRoot`.
4. Start and enable the web service.
5. Allow HTTP through the firewall.
6. Test the web page (it should fail due to SELinux context).
7. Use `semanage` to assign the correct SELinux file context for `/web`.
8. Apply the context changes using `restorecon`.
9. Test again and confirm the web page loads.

---
