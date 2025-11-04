# Connect to remote system
ssh USERNAME@x.x.x.x 

### x.x.x.x is the ip of the remote system you are connecting to

## Verify remote access
```
hostname
```

## Exit remote shell
exit

## Create local transfer directory
```
mkdir -p ~/remote_transfer
```

## Copy /etc/hosts to remote system's /tmp directory
```
scp /etc/hosts USERNAME@x.x.x.x:/tmp/
```

## Verify on remote system
```
ssh USERNAME@x.x.x.x "ls -l /tmp/hosts"
```
