#Dump large databases and restore from .gz files if necessary

Dump to a .gz file to save space:
```bash
mysqldump -u USER -p --single-transaction --quick --lock-tables=false DATABASE | gzip > OUTPUT.gz
```

And restore from .gz if necessary
```bash
gunzip < OUTPUT.gz | mysql -u USER -p DATABASE
```
