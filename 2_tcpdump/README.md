# supk42/tcpdump

This is dockerized version of tcpdump

# # What is tcpdump

tcpdump is packet analyzer.  http://tcpdump.org/ .

The easiest way to use `tcpdump` is to create an alias to call the container.

```bash
alias nmap='docker run -it --rm supk42/tcpdump'

tcpdump -host -port
```
