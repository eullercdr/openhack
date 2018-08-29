# openhack
OpenHack 2018

https://docs.microsoft.com/en-us/azure/container-instances/container-instances-tutorial-prepare-acr
https://docs.microsoft.com/en-us/azure/container-instances/container-instances-tutorial-deploy-app

## Create a Tag
docker tag repo acreullercristian.azurecr.io/minecraft
docker push acreullercristian.azurecr.io/minecraft

## List Images
az acr repository list --name acrEullerCristian --output table

az acr show --name acrEullerCristian --query loginServer
