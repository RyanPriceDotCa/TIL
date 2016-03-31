#Identify locked tables and unlock them

Command to check for locked tables:
```bash
show open tables where in_use>0;
```

Command to show process list:
```bash
show processlist;
```

One of the processes is locking the table.  To kill that process:
```bash
kill put_process_id_here;
```
