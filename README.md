# yugadb-demo

this is modified original instructions of https://docs.yugabyte.com/latest/quick-start/create-local-cluster/

## usage

```
k create ns yugabyte-demo
k apply -f yugabyte-statefulset-rf-1.yaml -n yugabyte-demo
k -n yugabyte-demo get all
k -n yugabyte-demo exec -it yb-master-0 bash --  -c "YB_ENABLED_IN_POSTGRES=1 FLAGS_pggate_master_addresses=yb-master-0.yb-masters.yugabyte-demo.svc.cluster.local:7100 /home/yugabyte/postgres/bin/initdb -D /tmp/yb_pg_initdb_tmp_data_dir -U postgres"
k -n yugabyte-demo port-forward service/yb-master-ui 7000:7000
```
