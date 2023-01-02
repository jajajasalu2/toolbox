## Git (Got)

### Selectively rollback unstaged changes

```
git checkout -p
```

### View changes from a higher-level

```
git log --oneline --stat
```

### Stage modified files

```
git diff -u --name-only | xargs git add
```

### Unstage changes (i.e. revert a git add, or a soft reset)

```
git reset
```

### Soft revert a change

If the change is on HEAD:

```
git reset --soft HEAD~
```

Then unstage the change:

```
git reset
```

### Track the entire history of a function or line(s)

As opposed to git blame which points to just the last commit.

```
git log -L line1,line2:path/to/file.c
git log -L :func_name:path/to/file.c
```

For example:

```
git log -L 3045,3094:net/tcp_ipv4.c
git log -L :tcp_v4_connect:net/tcp_ipv4.c
```
