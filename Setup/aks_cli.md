# Creazione Azure Services Principal
'''azure cli
az login
az account list

#get subscription ID
subscriptionID=$(az account show --query id -o tsv)

az ad sp create-for-rbac --name <name> \
                         --role <role> \
                         --scopes /subscriptions/$subscriptionID/resourceGroups/<rgname>
'''