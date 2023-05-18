---
title: "Ubuntu"
date: 2023-05-11T20:32:15+08:00
draft: false
---

## Install .deb

``` bash
sudo dpkg -i package-name.deb
```

## Set timezone

``` bash
timedatectl set-timezone Asia/Shanghai
```

## Change NTP server

1. Open and Edit the configuration file

    ``` bash
    vim /etc/systemd/timesyncd.conf
    ```

2. Add(Uncomment) NTP servers under the [Time] like following

    ``` bash
    [Time]
    NTP=10.0.0.1
    ```

3. Restart the service to apply the changes

    ```bash
    systemctl restart systemd-timesyncd.service
    ```

4. To check time sync status

   ``` bash
   timedatectl status
   ```

See also [How to change NTP server on Ubuntu 20.04.1 LTS simply](https://dannyda.com/2021/04/27/how-to-change-ntp-server-on-ubuntu-20-04-1-lts-simply-default-contents-of-etc-systemd-timesyncd-conf-on-ubuntu-20-04-1-lts/)
