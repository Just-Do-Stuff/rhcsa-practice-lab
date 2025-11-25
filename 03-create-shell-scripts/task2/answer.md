## Answer

```
#!/bin/bash

DIR=~/scripts_practice
REPORT=~/scripts_practice/report.txt
```

# Check directory exists
```
if [ ! -d "$DIR" ]; then
    echo "Directory not found: $DIR"
    exit 1
fi
```

# Empty report file before writing
> "$REPORT"

# Loop through directory contents
```
for file in "$DIR"/*; do
    if [ -f "$file" ]; then
        lines=$(wc -l < "$file")
        echo "File: $(basename "$file") - $lines lines" | tee -a "$REPORT"
    fi
done
```

---

## Notes
- Use `chmod +x scriptname.sh` to make scripts executable.
- Use `./scriptname.sh` to run scripts in the current directory.
- Always verify output after executing the script.
