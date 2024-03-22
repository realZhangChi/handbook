---
title: "Common Commands"
date: 2023-03-07T15:15:46+08:00
draft: false
---

## Rename branch

``` bash
git branch -m NEW_BRANCH_NAME
```

## Ignore local file modifications

``` bash
git update-index --no-skip-worktree /path/to/file
```

## Delete a Git branch locally

``` bash
git branch --delete <branchname>
```

See also [How to delete a Git branch locally](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/delete-local-git-branch-origin-force-merge-all).

## Update submodules recursively

``` bash
git submodule update --init --recursive
```

See also [Git update submodules recursively](https://stackoverflow.com/a/10168693)

## Config proxy

``` bash
git config --global https.proxy http://127.0.0.1:7890

git config --global https.proxy https://127.0.0.1:7890

git config --global --unset http.proxy

git config --global --unset https.proxy
```

See also [git 设置和取消代理](https://gist.github.com/laispace/666dd7b27e9116faece6#gistcomment-2026447)