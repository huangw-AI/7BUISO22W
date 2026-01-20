# 7BUISO22W Course

### This is the Module repository for the MSc Cyber Security Application. 

DNS reset and switching between university and home networks

Using NAT Outside the University (DNS and resolvconf)
Internet Connection Outside the University (NAT)

When working outside the university network, the Kali VM should use NAT for internet access.
Some activities require only the Kali VM to be online, which can be achieved using NAT mode.
The university-provided Kali image is configured for use inside the university network to avoid blocked Kali domains when updating repositories.
Therefore, when working outside the university premises, you must switch the DNS resolver to match your home network configuration.



# how to use switch-dns.sh

A simple Bash script to switch between different DNS configurations by replacing  
`/etc/resolv.conf` with predefined profiles (e.g. university vs home).

The script also locks the file to prevent NetworkManager or systemd from overwriting it.

---

## Requirements

- Linux  
- Root access (sudo)  
- `chattr` available  

---

## Setup

### 1. Create the script file

```bash
nano switch-dns.sh
```
On gitbub, click on the switch-dns.sh script, copy it and Paste the script content in the nano terminal, then press:
Ctrl + X
Y
Enter

to save and exit.
### 2. Make it executable
```bash
chmod +x switch-dns.sh
```
## Usage

### Switch to university DNS:
```bash
sudo ./switch-dns.sh uni
```
### Switch to home DNS:
```bash
sudo ./switch-dns.sh home
```

### Check current status:
```bash
sudo ./switch-dns.sh status
```

### Show current DNS configuration:
```bash
sudo ./switch-dns.sh show
```
