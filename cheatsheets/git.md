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
