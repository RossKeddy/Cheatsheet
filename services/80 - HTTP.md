
Directories
```
gobuster dir -u http://runner.htb/ -w /usr/share/wordlists/ -b "302,404" -t 50
```

Subdomains
```
gobuster dns -d runner.htb -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -t 50
```

vHosts
```
gobuster vhost -u runner.htb -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -t 50
```

FFUF
DNS
```
ffuf -w ~/wordlists/wordlists/SecLists/Discovery/DNS/subdomains-top1million-110000.txt:FUZZ -u http://FUZZ.board.htb/
```

vHost
```
ffuf -w ~/wordlists/wordlists/SecLists/Discovery/DNS/subdomains-top1million-110000.txt:FUZZ -u http://board.htb/ -H 'Host: FUZZ.board.htb' -fs 900
```