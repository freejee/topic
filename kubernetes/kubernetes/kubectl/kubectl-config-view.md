# kubectl config view

+ [概述](#%E6%A6%82%E8%BF%B0)
+ [用法](#%E7%94%A8%E6%B3%95)
+ [选项](#%E9%80%89%E9%A1%B9)
+ [示例](#%E7%A4%BA%E4%BE%8B)

## 概述

Display merged kubeconfig settings or a specified kubeconfig file.

You can use **`--output jsonpath={...}`** to extract specific values using a jsonpath expression.

## 用法

```
kubectl config view [flags] [options]
```

Use **`kubectl options`** for a list of global command-line options (applies to all commands).

## 选项

+ **`--allow-missing-template-keys=true`**: 
If **`true`**, ignore any errors in templates when a field or map key is missing in the template.
Only applies to golang and jsonpath output formats.

+ **`--merge=true`**: 
If **`true`**, merge the full hierarchy of kubeconfig files.

+ **`--flatten=false`**: 
If **`true`**, flatten the resulting kubeconfig file into self-contained output (useful for creating portable kubeconfig files).

+ **`--minify=false`**: 
If **`true`**, remove all information not used by current-context from the output.

+ **`--raw=false`**: 
If **`true`**, display raw byte data.

+ **`--output, -o='yaml'`**: 
Output format.
One of: **`json|yaml|name|go-template|go-template-file|template|templatefile|jsonpath|jsonpath-file`**.

+ **`--template=''`**: 
Template string or path to template file to use when **`-o=go-template`**, **`-o=go-template-file`**.
The template format is golang templates [http://golang.org/pkg/text/template/#pkg-overview].

## 示例

Show merged kubeconfig settings.
```
kubectl config view
```

Show merged kubeconfig settings and raw certificate data.
```
kubectl config view --raw
```

Get the password for the e2e user.
```
kubectl config view -o jsonpath='{.users[?(@.name == "e2e")].user.password}'
```


