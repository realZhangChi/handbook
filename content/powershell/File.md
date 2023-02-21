---
title: "File"
date: 2023-02-21T10:36:53+08:00
weight: 1
draft: false
---

## Extension

### System.IO.Path.GetExtension

``` bash
[System.IO.Path]::GetExtension(Draftv2.zip)
```

Returns the extension (including the period ".") of the specified path string. See also [M$ Learn](https://learn.microsoft.com/en-us/dotnet/api/system.io.path.getextension?view=net-7.0).

### FileSystemInfo.Extension

``` bash
> (Get-ChildItem Draftv2.zip).Extension
.zip
> (Get-Item Draftv2.zip).Extension
.zip
```

Gets the extension part of the file name, including the leading dot . even if it is the entire file name, or an empty string if no extension is present. See also [M$ Learn](https://learn.microsoft.com/en-us/dotnet/api/system.io.filesysteminfo.extension?view=net-7.0).

## Expand-Archive

``` bash
Expand-Archive -Path Draftv2.zip -DestinationPath C:\Reference
```

The Expand-Archive cmdlet extracts files from a specified zipped archive file to a specified destination folder. See also [M$ Learn](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.archive/expand-archive?view=powershell-7.3).
