---
title: "Daemon.json"
date: 2023-06-14T10:42:26+08:00
draft: false
---

## `/etc/docker/daemon.json`

``` json
{
    "data-root": "PATH_TO_YOUR_NEW_DOCKER_DATA_ROOT",
    "insecure-registries": ["IP_ADDRESS:PORT"],
    "log-driver":"json-file",
    "log-opts":{
        "max-size" :"50m","max-file":"1"
    }
}
```
