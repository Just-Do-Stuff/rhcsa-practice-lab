## Category 01 — Understand and Use Essential Tools
---

## Purpose

- This category focuses on the foundational Linux commands and tools that everything else on Red Hat Enterprise Linux is built on. 
- You will practice working at the command line, manipulating files and directories, using redirection and pipes, searching text, connecting remotely, and managing basic permissions.
- The goal is to make you confident and fast in the shell, since almost every RHCSA task assumes you are comfortable here.

---

## Tools Used

For consistency, tasks in this category primarily use:

- The shell (`bash`) and a terminal or console session 
- `ls`, `cd`, `pwd`, `cp`, `mv`, `rm`, `mkdir`, `rmdir` 
- Redirection and pipes: `>`, `>>`, `2>`, `2>&1`, and `|` 
- `grep` (with simple regular expressions) 
- `ssh` and `scp` for remote access and file transfer 
- `tar`, `gzip`, `bzip2` for archives and compression 
- `ln` for hard and soft links 
- `chmod`, `chown`, and `chgrp` for permissions 
- `man`, `info`, and files under `/usr/share/doc` for documentation

These commands form the core toolkit you will use in almost every other RHCSA category.

---

## VERY IMPORTANT: Working Safely in the Shell

> Many of the commands you practice here can permanently delete or overwrite data if used carelessly.

Keep these points in mind while working through the tasks:

- Always run `pwd` to verify where you are in the working directory.
- Use `ls` to verify files and paths before acting on them. 
- When practicing `rm`, use example directories in your home directory (for example, `~/lab/`) and avoid system paths like `/etc`, `/var`, or `/boot`. 
- When using `ssh` and `scp`, double-check the host, username, and path before pressing Enter.

Getting comfortable and staying safe at the shell is critical both for the exam and real-world administration.

---

## What You Will Practice

In this category, you will learn how to:

- Access a shell prompt and issue commands with correct syntax.
- Use input-output redirection (`>`, `>>`, `|`, `2>`, etc.) 
- Use `grep` and simple regular expressions to analyze text.
- Access remote systems using `ssh` and transfer files with `scp` 
- Log in and switch users in multiuser targets (`su`, `sudo`) 
- Archive, compress, unpack, and uncompress files using `tar`, `gzip`, and `bzip2` 
- Create and edit text files with your editor of choice.
- Create, delete, copy, and move files and directories.
- Create hard and soft links.
- List, set, and change standard `ugo/rwx` permissions.
- Locate and use system documentation (`man`, `info`, `/usr/share/doc`)

Each task is designed to isolate one or two of these objectives so you can practice them in a focused way.

---

**Recommended workflow:**

1. Go into a task directory. 
2. Open `instructions.md` and complete the task on your own. 
3. Only check `answer.md` after you have tried the task or if you get stuck.

---

## Tasks in This Category


### Task 1 – [Shell Access and Basic Commands](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task1)

You will practice:

- Opening a shell and confirming your current user and directory.
- Running basic commands with correct syntax.
- Navigating the filesystem with `cd`, `pwd`, and `ls`

---

### Task 2 – [Redirection and Pipes](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task2)

You will practice:

- Sending command output to a file using `>` and `>>` 
- Redirecting error output with `2>` 
- Combining streams and using pipes (`|`) to build simple command chains.

---

### Task 3 – [Text Searching with grep and Regular Expressions](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task3)

You will practice:

- Using `grep` to search for strings in files and command output.
- Using basic regular expressions (such as anchors and character classes).
- Counting matches and filtering relevant lines.

---

### Task 4 – [SSH Access and Remote Work](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task4)

You will practice:

- Connecting to a remote system with `ssh`.
- Running basic commands on a remote host.
- Using `scp` to copy files to and from a remote system.
- Verifying connectivity when you do and do not have a remote system available.

---

### Task 5 – [Logging In and Switching Users](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task5)

You will practice:

- Logging in as a regular user.
- Switching users with `su`
- Using `sudo` to run administrative commands.
- Confirming who you are with `whoami` and understanding effective UID.

---

### Task 6 – [Archiving and Compression](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task6)

You will practice:

- Creating and extracting archives with `tar`
- Compressing and uncompressing files with `gzip` and `bzip2`
- Combining `tar` and compression flags in a single command.

---

### Task 7 – [Create and Edit Text Files](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task7)

You will practice:

- Creating text files in your home directory.
- Editing content using an editor (such as `vim`, or `nano`)
- Verifying content with `cat`, `head`, or `tail`

---

### Task 8 – [File and Directory Management](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task8)

You will practice:

- Creating, copying, moving, and deleting files and directories.
- Using `mkdir -p`, `cp -r`, and `rm -r` in safe lab directories.
- Verifying structure changes with `ls -R`

---

### Task 9 – [Hard and Soft Links](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task9)

You will practice:

- Creating hard links with `ln`
- Creating symbolic links with `ln -s` 
- Understanding how changes to a source file affect linked files.

---

### Task 10 – [Permissions and Ownership](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools/task_10)

You will practice:

- Viewing file permissions with `ls -l` 
- Changing permissions with `chmod` (symbolic and numeric) 
- Adjusting ownership with `chown` and `chgrp` 
- Verifying that `ugo/rwx` settings behave as expected for different users.


