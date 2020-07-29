# Command to list sessions

```bash
sessions
sessions -i 'SESSION_NUMBER'  # target specific session
```

## Spool service

```bash
ps | grep spool
spoolsv.exe
```

## Migrate process

```bash
migrate 'PID'
```

## Check user who's the system is running

```bash
getuid
```

## Get info of the system

```bash
sysinfo
```

## Load wiki

```bash
load wiki  # previously known as mimikatz
```

## Get all privileges

```bash
getprivs # previously known as mimikatz
```

## Transfer file to the target

```bash
upload
```

## Run a Metasploit module

```bash
run
```

## Verify network interface

```bash
Linux: ifconfig
Windows: ipconfig
```

## Check if it's a VM

```bash
run post/windows/gather/checkvm
```

## Check for various exploits which we can run within our session

```bash
run post/windows/gather/checkvm
```

## Forcing RDP to be available

```bash
run post/windows/manage/enable_rdp
```

## Spawn a shell

```bash
shell
```

## Autoroute

```bash
run autoroute [-r] -s subnet -n netmask
run autoroute -s 172.18.1.0 -n 255.255.255.0
```

## Autoroute

```bash
auxiliary/server/socks4a
```

## Proxychain

```bash
auxiliary/server/socks4a
```
