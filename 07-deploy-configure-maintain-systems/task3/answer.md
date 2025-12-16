## Answer

```
crontab -e
# Example entry:
0 2 * * * /usr/bin/echo "cron job ran"
```

## Using at
```
echo "echo 'at job ran'" | at now + 1 minute
```

## Verify
crontab -l
atq
