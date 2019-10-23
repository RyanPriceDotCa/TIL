A couple ways to dump a database to/from a remote server:

Option #1 (from destination):
SSH tunnel to remote from local:
```bash
ssh -f -L3310:localhost:3306 user@remote.server -N
```
Dump remote to local after SSH runnel
```bash
mysqldump -P 3310 -h 127.0.0.1 -u mysql_user -p database_name table_name
```

Option #2 (from target):
```bash
mysqldump <DATABASE_NAME> [mysqldump options] | gzip -c | ssh user@remotehost "cat > /path/to/some-file.sql.gz"
```
