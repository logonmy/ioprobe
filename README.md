ioprobe
--------

サンプル

```bash
$ sudo ioprobe [pid]
date    rchar/s wchar/s syscr/s syscw/s read_bytes/s    write_bytes/s   cancelled_write_bytes/s
2015-02-28 00:11:36     0       0       0       0       0       0       0
2015-02-28 00:11:37     0       0       0       0       0       0       0

$ sudo ioprobe --json [pid]
{'write_bytes': 0, 'cancelled_write_bytes': 0, 'read_bytes': 0, 'date': '2015-02-28 00:12:15', 'syscr': 0, 'wchar': 0, 'rchar': 0, 'syscw': 0}
{'write_bytes': 0, 'cancelled_write_bytes': 0, 'read_bytes': 0, 'date': '2015-02-28 00:12:16', 'syscr': 0, 'wchar': 0, 'rchar': 0, 'syscw': 0}
```

コマンドの使い方は以下。

```bash
$ ioprobe -h
usage: ioprobe [-h] [--json] pid

I/O probe for process.

positional arguments:
  pid         target process's pid.

optional arguments:
  -h, --help  show this help message and exit
  --json      change command's output to JSON.
```
