---
title: "Npm"
date: 2024-04-03T14:35:18+08:00
draft: true
---


## Change the npm package registry

Temporary use: `npm --registry https://registry.npm.taobao.org install express`

Persistent use: `npm config set registry https://registry.npm.taobao.org`

Using cnpm: `npm install -g cnpm --registry=https://registry.npm.taobao.org`

Switch back to official registry: `npm config set registry https://registry.npmjs.org/`

Check current registry: `npm config get registry`

- See also [npm换源](https://www.jianshu.com/p/f311a3a155ff)

## Config proxy

``` bash
npm config set strict-ssl false

npm config set proxy http://127.0.0.1:7890

npm config set https-proxy http://127.0.0.1:7890

```

- See also [Is there a way to make npm install (the command) to work behind proxy?](https://stackoverflow.com/questions/7559648/is-there-a-way-to-make-npm-install-the-command-to-work-behind-proxy)
