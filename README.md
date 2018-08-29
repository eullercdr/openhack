# openhack
OpenHack 2018

https://docs.microsoft.com/en-us/azure/container-instances/container-instances-tutorial-prepare-acr
https://docs.microsoft.com/en-us/azure/container-instances/container-instances-tutorial-deploy-app

## Create a Tag
docker tag repo acreullercristian.azurecr.io/minecraft
docker push acreullercristian.azurecr.io/minecraft

## List Images
az acr repository list --name acrEullerCristian --output table

## Show login server
az acr show --name acrEullerCristian --query loginServer

## Show the password
az acr credential show --name acrEullerCristian --query "passwords[0].value"

## Make a deploy of container
az container create --resource-group myDockerImages --name minecraft-app --image acreullercristian.azurecr.io/minecraft --cpu 1 --memory 1 --registry-login-server acreullercristian.azurecr.io --registry-username acrEullerCristian --registry-password <password> --dns-name-label aci-demo --ports 80
