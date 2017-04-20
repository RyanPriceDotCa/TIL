#Recursively list files by last modified date

```bash
pwd | find $1 -type f -print0 | xargs -0 stat --format '%Y :%y %n' | sort -nr | cut -d: -f2- | head
```

where pwd can be whatever directory you want to search.
