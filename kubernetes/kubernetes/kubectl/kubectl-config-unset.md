# kubectl config unset

+ [概述](#%E6%A6%82%E8%BF%B0)
+ [用法](#%E7%94%A8%E6%B3%95)
+ [示例](#%E7%A4%BA%E4%BE%8B)

## 概述

Unsets an individual value in a kubeconfig file.

**`PROPERTY_NAME`** is a dot delimited name where each token represents either an attribute name or a map key.

Map keys may not contain dots.

## 用法

```
kubectl config unset PROPERTY_NAME [options]
```

Use **`kubectl options`** for a list of global command-line options (applies to all commands).

## 示例

Unset the current-context.
```
kubectl config unset current-context
```

Unset namespace in foo context.
```
kubectl config unset contexts.foo.namespace
```


