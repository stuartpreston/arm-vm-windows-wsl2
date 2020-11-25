# arm-vm-customregion

A quick ARM template to demonstrate installation of WSL2 in the OS customization phase (before the first user can logon). Based off the [101-vm-simple-windows Quickstart Template](https://github.com/Azure/azure-quickstart-templates/tree/master/101-vm-simple-windows)

## Usage

```sh
az group create --name demo-wsl2 -l westeurope
az deployment group create -g demo-wsl2 --template-file azuredeploy.json --parameters azuredeploy.parameters.json --parameters adminUsername=azureuser --parameters adminPassword=YOURADMINPASSWORD --parameters dnsLabelPrefix=sp2020112400
```

## Deleting the resources

```sh
az group delete -n demo-wsl2 --no-wait -y
```

## Author

Stuart Preston