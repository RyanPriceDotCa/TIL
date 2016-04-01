#Configure Postfix to only send emails

This will enable the mail() function to work, but doesn't use the full mail webserver.

Make sure all other mail servers are uninstalled, then run the following:

```bash
show open tables where in_use>0;
postconf -e "inet_interfaces = loopback-only"
/etc/init.d/postfix restart
```
