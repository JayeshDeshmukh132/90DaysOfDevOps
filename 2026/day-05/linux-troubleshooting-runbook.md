# Disk i/o commands

du -sh <file/folder> (Helps to find out file/dir size)
    -s is summary, -h helps display size 

Example - 
```
[jayeshdeshmukh@localhost Desktop]$ du -sh scripts/
20K     scripts/
[jayeshdeshmukh@localhost Desktop]$
```

**du vs df**
df displays overall file system size
example - 
```
[jayeshdeshmukh@localhost Desktop]$ df -h
Filesystem             Size  Used Avail Use% Mounted on
devtmpfs               4.0M     0  4.0M   0% /dev
tmpfs                  5.6G     0  5.6G   0% /dev/shm
tmpfs                  2.3G  9.3M  2.3G   1% /run
/dev/mapper/rhel-root   70G  9.1G   61G  13% /
/dev/sda1              960M  612M  349M  64% /boot
/dev/mapper/rhel-home  124G  1.4G  122G   2% /home
tmpfs                  1.2G  100K  1.2G   1% /run/user/1000
[jayeshdeshmukh@localhost Desktop]$
```

# Network command
nmap site/serverip 
lists down open ports of specified server/site
example 
```
[jayeshdeshmukh@localhost ~]$ nmap google.com
Starting Nmap 7.92 ( https://nmap.org ) at 2026-01-28 21:57 IST
Nmap scan report for google.com (142.250.195.14)
Host is up (0.0065s latency).
Other addresses for google.com (not scanned): 2404:6800:4009:817::200e
rDNS record for 142.250.195.14: del12s09-in-f14.1e100.net
Not shown: 998 filtered tcp ports (no-response)
PORT    STATE SERVICE
80/tcp  open  http
443/tcp open  https

Nmap done: 1 IP address (1 host up) scanned in 4.47 seconds
```

telnet site/server port
check connectivity to the server on specified port
```
[jayeshdeshmukh@localhost ~]$ telnet google.com 443
Trying 142.250.70.110...
Connected to google.com.
Escape character is '^]'
```

ss -tulnp 
check ports listening for local



# system command
systemctl list-units
Lists all services running/failed

systemctl status <service name>
get details along with service status - running/failed


# journalctl command (for logs debugging service)
journalctl -e
- lists all logs generated 
    -e lists latest logs

jouranlctl -u <servicename> -f
    lists logs particular to that service
    -f makes sure logs are seen live (restart service/debugging)

journalctl -b <id>
    to see logs during a specific boot


