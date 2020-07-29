# GoBuster

## Directory shell detection

```bash
gobuster dir -u http://<ip>:333 -w <word list location>
```

## Gobuster flag

```bash
-e  # Print the full URLS in the console
-u  # The target URL
-w  # Path to the wordlist
-U and -P  # Username and Password for Basic Auth
-p <x>  # Proxy to use for requests
-c <http cookies>  # Specify a cookie for simulating the auth
```
