# Azure functions on Linux Preview
(based on https://blogs.msdn.microsoft.com/appserviceteam/2017/11/15/functions-on-linux-preview/)


## Create a Linux VM
Either in the portal or API

## Connect to the Linux VM using SSH
``` 
ssh adamstephensen@52.187.183.175
```

## Add Azure CLI 2.0 to a linux machine

- Install the Azure CLI 2.0 https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest

- Modify the courses list
```
echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
     sudo tee /etc/apt/sources.list.d/azure-cli.list
```	

- Run the following Sudo commands

```
sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
sudo apt-get install apt-transport-https
sudo apt-get update && sudo apt-get install azure-cli
```	


- Run the Azure CLI with the ```az``` Command

## Upgrade the Azure CLI

- upgrade just the Azure CLI

```
sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
```


- upgrade all of the installed packages which have not had a dependency change

```
sudo apt-get update && sudo apt-get upgrade

```

