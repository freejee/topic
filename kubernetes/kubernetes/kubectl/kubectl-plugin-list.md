# kubectl plugin list

+ [概述](#%E6%A6%82%E8%BF%B0)
+ [用法](#%E7%94%A8%E6%B3%95)
+ [选项](#%E9%80%89%E9%A1%B9)

## 概述

List all available plugin files on a user's PATH.

Available plugin files are those that are: - executable - anywhere on the user's PATH - begin with **`kubectl-`**

## 用法

```
kubectl plugin list [flags] [options]
```

Use **`kubectl options`** for a list of global command-line options (applies to all commands).

## 选项

+ **`--name-only=true`**: 
If true, display only the binary name of each plugin, rather than its full path.


