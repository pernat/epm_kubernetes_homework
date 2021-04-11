HomeWork part #1

• Create namespace monitoring
• Create service account grabber in that namespace
• Create role that can get, list, watch on all Pods in the cluster


### Step 1
```bash
kubectl apply -f monitoring_ns.yaml
```
### Step 2
```bash
kubectl apply -f grabber_sa.yaml
```
### Step 3
```bash
kubectl apply -f role.yaml
```
### Step 4
```bash
kubectl create clusterrolebinding pod-access --clusterrole=pod-access --serviceaccount=monitoring:grabber
```
### Step 5
```bash
kubectl auth can-i get pods -A --as system:serviceaccount:monitoring:grabber
kubectl auth can-i create pods -A --as system:serviceaccount:monitoring:grabber
```

