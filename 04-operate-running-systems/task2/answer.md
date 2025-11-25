## Answer


# 1. Top 5 CPU processes
```
ps -eo pid,ppid,cmd,%cpu --sort=-%cpu | head -n 6
```

# 2. Top 5 memory processes
```
ps -eo pid,ppid,cmd,%mem --sort=-%mem | head -n 6
```

# 3. Kill a process
```
kill <PID>
```

# 4. Start process with a lower priority
```
nice -n 10 <command>
```

# 5. Adjust existing process priority
```
sudo renice 5 <PID>
```

# 6. List tuning profiles
```
sudo tuned-adm list
```

# 7. Activate performance profile
```
sudo tuned-adm profile performance
```
