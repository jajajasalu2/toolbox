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
