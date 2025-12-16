# RHCSA Supplement Practice Tasks - RHEL 10

## Purpose

This repository provides hands-on, exam-style exercises for each RHCSA objective. 
It’s designed so you can practice tasks in a way that feels like you are taking the exam. 

Each objective is organized into:

- Exam-style tasks (`instructions.md`) 
- Corresponding answers (`answer.md`) 
- Folders grouped by exam category, each with its own `README.md`
- Each category corresponds with a RHCSA exam Category. Which can be found here: [RHCSA Exam Objectives](https://www.redhat.com/en/services/training/ex200-red-hat-certified-system-administrator-rhcsa-exam) 

---

## How the Repo Is Structured

- The root of the repo contains this README and top-level category folders. 
- Each category (for example, `01-understand-essential-tools/`, `02-manage-software/`) contains:
  - A `README.md` that explains:
    - What the category covers 
    - Important warnings / notes 
    - How the tasks are organized
- Inside each category, tasks are stored in subfolders, for example:

  ```
  01-understand-essential-tools/
  └── task1-basic-shell/
      ├── instructions.md
      └── answer.md
  ```

---

## IMPORTANT!

It is very normal and expected to get stuck on a task as you are learning. That is where the growth and those AH HA moments happen.

The ONLY items available for use on the RHCSA exam will be:

- The `man` pages and
- `--help` flags 

> Do NOT rely on ChatGPT or any external assistant while you are actually practicing.
## ChatGPT will not be there with you on the exam.

---

## Recommended Environment

For the best experience and to match RHCSA-style setups:

- Use at least two VMs:
  - One as your primary practice system
  - One as a **second system** for:
    - SSH practice  
    - `scp` file transfers  
    - NFS and other network-based tasks
- Obtain the RHEL 10 iso. It's free with a developer account. [Go Here](https://developers.redhat.com/products/rhel/download)

You can use any hypervisor (VirtualBox, VMware, KVM, Proxmox, etc.) as long as both VMs can reach each other over the network.

If you dont have a reliable pc, you can use labex.io. However, I am not sure if you are able to clone repos there. 

---

# How to Use This Repo

## 1. Clone this repository:

   ```
   git clone https://github.com/Just-Do-Stuff/rhcsa-practice-lab.git
   cd rhcsa-practice-lab
   ```

## 2. Start with the first exam category 
   Go to [`01-understand-essential-tools/`](https://github.com/Just-Do-Stuff/rhcsa-practice-lab/tree/main/01-understand-essential-tools) and:

   - **Read the `README.md` first.** 
     It explains the goals, tools, and important notes for that category.
   - Please make sure you are reading the README for each category.

## 3. Then go task by task inside the category

   For each task directory:

   1. Open `instructions.md` 
      - Read the scenario carefully. 
      - Perform the task on your own.

   2. **Do NOT** open `answer.md` yet.
      - Try to solve the task using `man`, `--help`, and your notes. 
      - If you get stuck, troubleshoot like you would on the exam.
      - If you have no clue about the task, use your notes and the web( but dont make this a habit)
      - Truly understand what the task is asking you.

   3. Only after you’ve made a real attempt, open `answer.md`
      - Compare your solution with the reference commands. 
      - Re-run the task if needed until it feels comfortable.

# 4. **Repetition is the point**

   > Each task should be done **at least 20 times**. Yes I said that route at least 20 times. You have to get your reps in with anything new. There are no shortcuts. Plus this will greatly help you during your interviews!

   The goal is for the commands and workflows to feel automatic under time pressure. 
   By the 20th repetition, you should be able to complete the task quickly and without checking notes.

---

## Study Discipline

To get the most out of this lab:

- Treat every task like a real RHCSA exam question. 
- Time yourself occasionally to simulate exam pressure. 
- Avoid copy-pasting commands; type them out. There is 0 critical thinking happening when you copy and paste. Respect yourself and just avoid it!
- If something breaks, don’t reset immediately—try to fix it using logs, `journalctl`, and `man` pages.
- Study for at least 3 hours a day. Go longer during the weekends.

---

## Disclaimer

All questions, tasks, and examples in this repo were created solely to help with RHCSA studies for supplemental studies.
This repo does **not** contain any proprietary Red Hat exam material and is not affiliated with Red Hat in any way.
