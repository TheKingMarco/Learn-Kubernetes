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
# Creazione ACR
```azure cli
$ACRNAME="learn-acr"

az acr create --resource-group myResourceGroup --name $ACRNAME --sku Basic

###Login acr
az acr login --name $ACRNAME

```