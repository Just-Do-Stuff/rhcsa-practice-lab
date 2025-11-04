#Connect to remote system
ssh admin@192.168.10.10

# Once connected (on remote):
hostname
exit

# Back on local system
mkdir -p remote_transfer

# Secure copy example
scp /etc/hosts admin@192.168.10.10:/tmp/

# Verify the file transfer (back on remote)
ssh admin@192.168.10.10 "ls -l /tmp/hosts"
