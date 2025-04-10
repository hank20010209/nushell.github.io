---
title: kill
categories: |
  platform
version: 0.103.0
platform: |
  Kill a process using the process id.
usage: |
  Kill a process using the process id.
editLink: false
contributors: false
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `kill` for [platform](/commands/categories/platform.md)

<div class='command-title'>Kill a process using the process id.</div>

## Signature

```> kill {flags} (pid) ...rest```

## Flags

 -  `--force, -f`: forcefully kill the process
 -  `--quiet, -q`: won't print anything to the console
 -  `--signal, -s {int}`: signal decimal number to be sent instead of the default 15 (unsupported on Windows)

## Parameters

 -  `pid`: Process id of process that is to be killed.
 -  `...rest`: Rest of processes to kill.


## Input/output types:

| input   | output |
| ------- | ------ |
| nothing | any    |

## Examples

Kill the pid using the most memory
```nu
> ps | sort-by mem | last | kill $in.pid

```

Force kill a given pid
```nu
> kill --force 12345

```

Send INT signal
```nu
> kill -s 2 12345

```
