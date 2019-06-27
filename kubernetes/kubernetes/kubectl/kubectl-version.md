# kubectl version

+ [概述](#%E6%A6%82%E8%BF%B0)
+ [用法](#%E7%94%A8%E6%B3%95)
+ [选项](#%E9%80%89%E9%A1%B9)
+ [示例](#%E7%A4%BA%E4%BE%8B)

## 概述

Print the client and server version information for the current context.

## 用法

```
kubectl version [flags] [options]
```

Use **`kubectl options`** for a list of global command-line options (applies to all commands).

## 选项

+ **`--client=true`**: 
Client version only (no server required).

+ **`--short=true`**: 
Print just the version number.

+ **`--output, -o=''`**: 
One of **`yaml`** or **`json`**.

## 示例

Print the client and server versions for the current context.
```
kubectl version
```


