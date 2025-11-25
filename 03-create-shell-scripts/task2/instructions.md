# Task 2 — Looping Through Files and Directories

## Instructions

1. Create a directory named `~/scripts_practice`.
2. Inside that directory, create three files:
   - `file1.txt`
   - `file2.txt`
   - `file3.txt`
3. Add 2–4 lines of text to each file.
4. Write a shell script named `report.sh` that:
   - Loops through all items in `~/scripts_practice`
   - Processes only regular files
   - Prints the filename
   - Prints how many lines each file contains
   - Appends results to `~/scripts_practice/report.txt`
5. If the directory does not exist, the script should exit with an error. (avoid infinite loops)
