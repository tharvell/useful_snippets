# Cheet sheet

https://kubernetes.io/docs/reference/kubectl/cheatsheet/




# Kubectl Version

```bash
kubectl version
```

# List unique containers in deployment 
```bash 
 kubectl get pods --all-namespaces -o jsonpath="{..image}" |tr -s '[[:space:]]' '\n' |sort |uniq -c
```

# Get the status of kubernetes components
```bash
kubectl get componentstatuses
```

# List all the things kubernetes is doing

```bash
kubectl get all
```


# Cluster information

```bash
kubectl cluster-info
```

# List nodes in the cluster 

```bash
kubectl get nodes
```

# Node details 

```bash
kubectl describe nodes node-name
```

# List deployments 

```bash 
kubectl get deployments
```

# Delete a resources 
```bash 
kubectl delete thing_name
```

# Expose the cluster 
```bash
kubectl proxy
```
