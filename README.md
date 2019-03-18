# arm-multi-vm

Deploy multiple VMs

First create a resource group. Replace RESOURCEGROUP below. As LOCATION use westeurope, northeurope or other valid location names.

az group create -n RESOURCEGROUP -l LOCATION

Modify azuredeploy.parameters.json with the VNET name, VNET resource group and SUBNET to deploy to.

az group deployment create -g RESOURCEGROUP --template-file azuredeploy.json --parameters @azuredeploy.parameters.json
