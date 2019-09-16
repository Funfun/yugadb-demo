# yugadb-demo

this is modified original instructions of https://docs.yugabyte.com/latest/quick-start/create-local-cluster/

## usage

```
k create ns yugabyte-demo
k apply -f yugabyte-statefulset-rf-1.yaml -n yugabyte-demo
k -n yugabyte-demo get all
```
