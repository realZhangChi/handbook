---
title: "Common"
date: 2023-05-15T20:32:32+08:00
draft: false
---

## Delete files older than x days

```bash
find /path/to/files* -mtime +5 -exec rm {} \;
```

See also [Delete Files Older Than x Days on Linux](https://www.howtogeek.com/288/delete-files-older-than-x-days-on-linux/).

## View systemd logs

``` bash
journalctl -u service-name.service
```

See also:

- [How to see full log from systemctl status service?](https://unix.stackexchange.com/questions/225401/how-to-see-full-log-from-systemctl-status-service)
- [How To Use Journalctl to View and Manipulate Systemd Logs
](https://www.digitalocean.com/community/tutorials/how-to-use-journalctl-to-view-and-manipulate-systemd-logs)

## Find directories that take up a lot of space

``` bash
du -h -d 1 <PATH> | sort -hr
```

See also [Linux磁盘占满问题分析步骤](https://blog.csdn.net/uestcyms/article/details/102475229).
