# supk42/nmap

This is dockerized version of Nmap.

# # What is nmap

nmap is free port analyzer.  http://nmap.org/ .

The easiest way to use `nmap` is to create an alias to call the container.

```bash
alias nmap='docker run -it --rm supk42/nmap'

nmap -sS yourIpAddress
```
source for alias : https://github.com/healthagentech/docker-nmap
