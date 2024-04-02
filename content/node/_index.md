---
title: "Node"
date: 2024-04-02T17:59:17+08:00
draft: false
---

## Change the npm package registry

Temporary use: `npm --registry https://registry.npm.taobao.org install express`

Persistent use: `npm config set registry https://registry.npm.taobao.org`

Using cnpm: `npm install -g cnpm --registry=https://registry.npm.taobao.org`

Switch back to official registry: `npm config set registry https://registry.npmjs.org/`

Check current registry: `npm config get registry`

- See also [npm换源](https://www.jianshu.com/p/f311a3a155ff)
