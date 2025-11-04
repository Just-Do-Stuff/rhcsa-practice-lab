Answer (task3/answer.md)


# Create the file
```cat <<EOF > /home/student/practice/users.txt
alice:x:1001:1001:Alice:/home/alice:/bin/bash
bob:x:1002:1002:Bob:/home/bob:/bin/bash
carol:x:1003:1003:Carol:/home/carol:/sbin/nologin
dave:x:1004:1004:Dave:/home/dave:/bin/bash
EOF
```

# Lines containing /bin/bash
grep "/bin/bash" ~/practice/users.txt > ~/practice/bash_users.txt

# Lines starting with 'b'
grep "^b" ~/practice/users.txt > ~/practice/b_users.txt
```
