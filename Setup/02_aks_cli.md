# Autenticazione
```azure cli
az login
az account list
```
# Creazione RG
```azure cli
$RGNAME="learn-kubernetes"
$LOCATION="westeurope"

az group create --name $RGNAME --location $LOCATION
```
# Creazione cluster aks
```azure cli
$AKSNAME="learn-aks-cluster"

az aks create -g $RGNAME -n $AKSNAME --enable-managed-identity --node-count 1

###install kubectl local###
az aks install-cli

###connessione al cluster aks###
az aks get-credentials --resource-group $RGNAME --name $AKSNAME

###verifica connessione###
kubectl get nodes
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
