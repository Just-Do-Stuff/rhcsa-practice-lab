## 🧠 Task 3

**Exam Category:** Understand and Use Essential Tools 
**Exam Objective:** Use grep and regular expressions to analyze text 

**Purpose:** 
To learn how to filter text using `grep` and basic regular expressions.

### Instructions
1. In your `~/practice` directory, create a file named `users.txt`. 
2. Add the following content: 
```
    alice:x:1001:1001:Alice:/home/alice:/bin/bash
    marcus:x:1002:1002:Marcus:/home/marcus:/bin/bash
    denise:x:1003:1003:Denise:/home/denise:/sbin/nologin
    mike:x:1004:1004:Mike:/home/mike:/bin/bash
```

3. Use `grep` to display only lines that contain `/bin/bash`. 
4. Then, use a regular expression to display lines that start with the letter **b**. 
5. Redirect each result to its own file (`bash_users.txt` and `b_users.txt`).
