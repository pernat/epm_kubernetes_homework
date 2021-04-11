HomeWork part #2

• Deploy any Stateful application on Kubernetes as StatefulSet. If you have no ideas, you can use minio.


### Step 1
```bash
kubectl create -f postgres-config.yaml
```

### Step 2
```bash
kubectl create -f postgres-service.yaml
```

### Step 3
```bash
kubectl create -f postgres-stateful.yaml
```
