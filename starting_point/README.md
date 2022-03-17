[HTB] Meow

Config:
```bash
$ export IP=<machine_ip>
```


NMAP scan results:
- `Telnet` service is open on port.

Connect to `root` with `telnet` on port 23:
```bash
$ telnet -l root -4 $IP
```
Seen a flat in the `/root`. Yank it and we're done!
