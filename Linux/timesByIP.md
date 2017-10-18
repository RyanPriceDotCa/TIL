Search through apache logs and show how many times various IPs show up

```bash
cat /var/log/apache2/some_apacheLog.log | cut -d' ' -f1 | sort | uniq -c | sort -n
```

where some_apache_log can be whatever log you want to search.
