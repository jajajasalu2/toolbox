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
