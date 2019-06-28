# kubectl config use-context

+ [概述](#%E6%A6%82%E8%BF%B0)
+ [别名](#%E5%88%AB%E5%90%8D)
+ [用法](#%E7%94%A8%E6%B3%95)
+ [示例](#%E7%A4%BA%E4%BE%8B)

## 概述

Sets the current-context in a kubeconfig file.

## 别名

+ use-context
+ use

## 用法

```
kubectl config use-context CONTEXT_NAME [options]
```

Use **`kubectl options`** for a list of global command-line options (applies to all commands).

## 示例

Use the context for the minikube cluster.
```
kubectl config use-context minikube
```  


