# kubectl rollout

+ [Overview](#overview)
+ [Usage](#usage)
+ [Available Commands](#available-commands)
+ [Options](#options)
+ [Examples](#examples)

## Overview
## Usage
## Available Commands
## Options
## Examples

## Overview

Manage the rollout of a resource.

Valid resource types include:
+ deployments
+ daemonsets
+ statefulsets

## Usage

```
kubectl rollout SUBCOMMAND [options]
```

Use **`kubectl <command> --help`** for more information about a given command.

Use **`kubectl options`** for a list of global command-line options (applies to all commands).

## Available Commands

```
history  View rollout history
pause    Mark the provided resource as paused
resume   Resume a paused resource
status   Show the status of the rollout
undo     Undo a previous rollout
```

## Examples

Rollback to the previous deployment
```
kubectl rollout undo deployment/abc
```

Check the rollout status of a daemonset
```
kubectl rollout status daemonset/foo
```


