# Inspection Commands
```azure cli

kubectl cluster-info                        # info about running kubernetes cluster
kubectl config get-clusters                 # list all the cluster available
kubectl config get-contexts                 # get all the contexts and the running one
kubectl config use-context <name-cluster>   # switch to kind context
kubectl get node                            # get nodes alias
kubectl get all                             # In addition to pods, we see services, daemonsets, deployments and replicasets

```

# Start Commands
```azure cli


az login
az aks get-credentials --resource-group   --name 

```

# Delete or Stop or start cluster AKS
```azure cli

az aks start -g $RGNAME -n $AKSNAME 

az aks stop -g $RGNAME -n $AKSNAME 

az aks delete -g $RGNAME -n $AKSNAME -y  #-y per confermare

###Delete the specified cluster from the kubeconfig.
kubectl config delete-cluster $AKSNAME
###Delete the specified context from the kubeconfig.
kubectl config delete-context $AKSNAME

```