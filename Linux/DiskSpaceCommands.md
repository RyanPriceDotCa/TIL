Show disk space used:

```bash
df -h
```

Show biggest directories:

```bash
du -hs * | sort -rh | head -30
```

Show the biggest files:

```bash
find -type f -exec du -Sh {} + | sort -rh | head -n 15
```
