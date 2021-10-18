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

[Comprehensive tutorial on the basics of firmware emulation. Check out all the links in here.](https://www.zerodayinitiative.com/blog/2020/5/27/mindshare-how-to-just-emulate-it-with-qemu)

[Stackexchange](https://reverseengineering.stackexchange.com/questions/4480/emulate-tp-link-wr740n-with-qemu)
