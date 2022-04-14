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
