# Nix

### Find executable files on a system

```
find . -exec file {} \;
```

then grep it for whatever, for example

```
find . -exec file {} \; | grep -i "elf 32-bit lsb"
```

### SSH with different algorithm

If the server gives a limited set of options for the key exchange algorithm:

```
ssh -oKexAlgorithms=+diffie-hellman-group1-sha1 root@192.168.0.1
```

### Difference between two directories

```
diff -qr dir1 dir2
```

### Setup an HTTP Server

Python2:

```
python -m SimpleHTTPServer --directory whatever 8080
```

Python3:

```
python -m http.server --directory whatever 8080
```

### Recursively download a directory from a server

[Stackoverflow](https://stackoverflow.com/questions/273743/using-wget-to-recursively-fetch-a-directory-with-arbitrary-files-in-it)

```
wget -r -np -R "index.html*" http://example.com/configs/.vim/
```

### Compare text files word-to-word

```
wdiff file1.txt file2.txt
```

### Checking hardware & system information

[Medium link](https://medium.com/technology-hits/basic-linux-commands-to-check-hardware-and-system-information-62a4436d40db)

```
uname -a
lscpu
lshw
hwinfo
lsscsi
lsusb
lsblk
df -H
cat /proc/cpuinfo
inxi -F
```

### Blacklist a kernel module

Get the module name using lsmod, then add it to `/etc/modprobe/blacklist.conf` like so:

```
blacklist <module_name>
```

one-liner:

```
echo "blacklist <module_name>" >> /etc/modprobe/blacklist.conf
```

Can't add disparaging comments about why the module is awful with the above though XD


### Make a directory writable and "sticky"

“Sticky” means that even if multiple users have write permission on a directory, only the owner of a file can delete the file within a sticky directory. (src: LFS v11.1).

```
chmod -v a+wt <dir>
```
