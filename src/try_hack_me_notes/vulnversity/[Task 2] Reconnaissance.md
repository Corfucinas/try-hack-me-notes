# Vulnversity

## Nmap

```bash
nmap -sV <machines ip>
-sV  # Attempts to determine the version of the services running
-p <x> or -p-  # Port scan for port or scan all ports
-Pn  # Disable host discovery and just scan for open ports
-A  # Enable OS and versio detection, executes in-build scripts for further enumeration
-sC  # Scan with the default nmap scripts
-v  # Verbose mode
-sU  # UDP port scan
-SS  # TCP SYN port scan
```
