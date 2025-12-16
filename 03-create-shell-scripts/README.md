## Category 03 — Create Simple Shell Scripts

---

## Purpose

- This category focuses on writing and running basic shell scripts.
- The goal is to help you practice the core scripting skills that may appear on the exam.
- We will work with arguments, conditionals, loops, and command output in simple, practical scripts.
- You will not build anything overly complex here—just small, focused scripts.


You are free to use any editor, but your scripts should always be executable and runnable directly from the command line.

---

## VERY IMPORTANT: Making Scripts Executable

Shell scripts will not run like normal commands unless they:

1. Have a valid shebang on the first line: #!/bin/bash

2. Are marked as executable:
   ```
   chmod +x scriptname.sh
   ```
3. Are run with a correct path, for example:
   ```
   ./scriptname.sh
   ```

Forgetting to add the shebang or execute permission is one of the most common issues when your script doesnt run.

---

## What You Will Practice

In this category, you will learn how to:
- Conditionally execute code using `if`, `test`, and `[ ]` 
- Use `for` loops to iterate over files and directories. 
- Read and use script parameters (`$1`, `$2`, etc.) 
- Capture and process the output of shell commands inside a script. 
- Write small, task-focused scripts that solve specific problems.

Each practice script is designed to be short and realistic, so you can quickly test and repeat until the logic feels natural.

---


**Recommended workflow:**

1. Read `instructions.md`. 
2. Create and test your own script **without** looking at the answer. 
3. Once done, open `answer.md` and compare your solution with the reference implementation.

---

## Tasks in This Category

### Task 1 – User-Based Script (Arguments and Conditionals)

You will practice:

- Accepting a username as a command-line argument(`$1`) 
- Checking whether the user exists using tools like `getent passwd` 
- Displaying information about the user (such as home directory and default shell) 
- Using conditional logic to print different messages and exit codes based on whether the user exists.



---

### Task 2 – Looping Through Files and Directories

You will practice:

- Looping through files in a directory using a `for` loop.
- Testing whether a path is a regular file before acting on it.
- Counting lines in each file using `wc -l` 
- Printing results to the screen and appending them to a report file.
- Handling basic error conditions (such as a missing directory)

