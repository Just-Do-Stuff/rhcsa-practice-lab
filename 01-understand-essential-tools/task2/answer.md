# Create the numbers file
```seq 1 10 > ~/practice/numbers.txt
```

# Redirect cat output to a new file
```
cat ~/practice/numbers.txt > ~/practice/output.txt
```

# Use a pipeline and redirect the result
```
cat ~/practice/numbers.txt | wc -l > ~/practice/count.log
```
