# SSH Practice Without a Remote System (Localhost Simulation)

---

## Purpose
If you don’t have access to a second system or virtual machine, you can still practice SSH commands locally by using your own machine as both the **client** and **server**. 

---

## INSTRUCTIONS

Follow these steps to simulate SSH connectivity, file transfer, and verification using your own system (localhost).

### Step 1: Install and Start SSH Service
```
sudo dnf install -y openssh-server
sudo systemctl enable --now sshd
sudo systemctl status sshd
```

### Step 2: Find Your Local IP or Hostname
```
hostname -I
hostname
```

### Step 3: Connect to Yourself Using SSH
```
ssh USERNAME@localhost
### OR

ssh USERNAME@127.0.0.1

```

## USERNAME=who you are currently logged in as
Then verify connection with:
```
hostname
```
Exit when done:
```
exit
```

### Step 4: Create a Directory and Transfer a File
```
mkdir -p ~/remote_transfer
scp /etc/hosts USERNAME@localhost:/tmp/
```

### Step 5: Verify File Transfer
```
ssh USERNAME@localhost "ls -l /tmp/hosts"
```
