# Reverse Engineering

## Pulling rootfs from a firmware image

Use binwalk

Get some info on the image

```
binwalk --signature --term image.img
```

Extract rootfs

```
binwalk -e image.img
```

## Emulating a router from a firmware image

[Stackexchange](https://reverseengineering.stackexchange.com/questions/4480/emulate-tp-link-wr740n-with-qemu)
