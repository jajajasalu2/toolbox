# Hackeroni Maccaroni

### Masscan scan all ports

```
sudo masscan -p1-65535,U1:65535 <target_ip> --rate=1000 -e <interface>
```

### Transfer files w/ Netcat

[Link](https://nakkaya.com/2009/04/15/using-netcat-for-file-transfers/)

Receiving machine:

```
nc -lp 1337 > out.file
```

Sending machine:

```
nc -w 3 <receiving-ip-addr> 1337 < in.file
```
