---
title: "Common Commands"
date: 2023-02-21T15:01:13+08:00
weight: 1
draft: false
---

## cp

Copy files/folders between a container and the local filesystem. See also [Docker Documentation](https://docs.docker.com/engine/reference/commandline/cp/).

``` bash
docker cp ./some_file CONTAINER:/work
docker cp CONTAINER:/var/logs/ /tmp/app_logs
```
