
# Ensure an argument was provided
```
if [ -z "$USERCHECK" ]; then
    echo "Usage: $0 <username>"
    exit 1
fi
```

# Check if user exists
```
if getent passwd "$USERCHECK" > /dev/null; then
    HOMEDIR=$(getent passwd "$USERCHECK" | cut -d: -f6)
    SHELL=$(getent passwd "$USERCHECK" | cut -d: -f7)

    echo "User exists."
    echo "Home Directory: $HOMEDIR"
    echo "Default Shell: $SHELL"
    exit 0
else
    echo "User '$USERCHECK' does not exist."
    exit 1
fi
```
