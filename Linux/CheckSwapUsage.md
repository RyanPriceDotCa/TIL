Show swaps happening:

```bash
vmstat 3 100
```

```
Will give a table like:
procs                  memory    swap         io     system         cpu
 r  b swpd   free  buff cache si   so   bi    bo   in    cs us sy id wa
 1  0    0 972488  7148 20848  0    0  856     6  138    53  0  0 99  0
 0  1    0 962204  9388 20848  0    0  747     0 4389  8859 23 24 11 41
 0  1    0 959500 10728 20848  0    0  440   313 1496  2345  4  7  0 89
 0  1    0 956912 12216 20848  0    0  496     0 2294  4224 10 13  0 77
 1  1    0 951600 15228 20848  0    0  997   264 2241  3945  6 13  0 81
 0  1    0 947860 17188 20848  0    0  647   280 2386  3985  9  9  1 80
 0  1    0 944932 19304 20848  0    0  705     0 1501  2580  4  9  0 87
```

The fields si and so show the amount of memory paged in from disk and paged out to disk, respectively. If the server shows continuous swap activity then more memory should be added or the SGA size should be reduced.
