# Azure CLI Virtual Machine 'vm' Command 
(based on https://docs.microsoft.com/en-us/cli/azure/vm?view=azure-cli-latest)


## Connect to the Jump box using SSH (if required)
``` 
ssh adamstephensen@52.187.183.175

ssh adamstephensen@adams-az-cli-2.australiaeast.cloudapp.azure.com

```


## Login to the Azure CLI

Reference: https://docs.microsoft.com/en-us/cli/azure/authenticate-azure-cli?view=azure-cli-latest

To use the interactive login (and then go to  https://aka.ms/devicelogin  )

```
az login
```
or

```
az login -u <username> -p <password>
```

or (recommended) use a service principal 

```
az login --service-principal -u <user> -p <password-or-cert> --tenant <tenant>
```

## Start the VM

```
az vm start -g adams-dev-vm-rg -n adams-vs2017-vm --no-wait
```

## Configure the DNS for the VM
(todo)

## Connect to the VM
RDP to the machine. e.g. adams-vs2017.australiaeast.cloudapp.azure.com:3389

## Stop the VM

```
az vm stop -g adams-dev-vm-rg -n adams-vs2017-vm --no-wait
```
