# kubectl explain

List the fields for supported resources

This command describes the fields associated with each supported API resource. Fields are identified via a simple JSONPath identifier:

```
<type>.<fieldName>[.<fieldName>]
```

Add the --recursive flag to display all of the fields at once without descriptions. Information about each field is retrieved from the server in OpenAPI format.

Use **`kubectl api-resources`** for a complete list of supported resources.

+ [Usage](#usage)
+ [Options](#options)
+ [Examples](#examples)

## Usage:

```
kubectl explain RESOURCE [options]
```

Use **`kubectl options`** for a list of global command-line options (applies to all commands).

## Options:

+ **`--api-version=''`**:
Get different explanations for particular API version

+ **`--recursive=false`**:
Print the fields of fields (Currently only 1 level deep)

## Examples:

Get the documentation of the resource and its fields

```
kubectl explain pods
```
  
Get the documentation of a specific field of a resource

```
kubectl explain pods.spec.containers
```


