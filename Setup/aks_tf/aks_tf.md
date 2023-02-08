# Autenticazione
```azure cli
az login
az account list
```
# Creazione Azure Services Principal
```azure cli
#get subscription ID
$subscriptionID=$(az account show --query id -o tsv)

#sp a livello subscription
az ad sp create-for-rbac --name sp-all-env --role Contributor --scopes /subscriptions/$subscriptionID

#sp a livello rg
az ad sp create-for-rbac --name sp-all-env --role Contributor --scopes /subscriptions/$subscriptionID/resourceGroups/$RGNAME

###conserva l'output del comando e inseriscilo nelle variabili sell Services Principal###
```