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
