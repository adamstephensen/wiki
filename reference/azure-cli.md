# Azure CLI 2.0 References


[Create a Linux virtual machine with the Azure CLI](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-cli)


## Start and stop a vm

```
az vm start --resource-group dev-vms --name vs2017-4

az vm deallocate --resource-group dev-vms --name vs2017-4
```

## Get a list of the available VM Sizes

```
az vm list-vm-resize-options --resource-group myResourceGroup --name myVM --output table
```

## Resize a VM

[How to resize a vm](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/change-vm-size)


```
az vm resize --resource-group myResourceGroup --name myVM --size Standard_DS3_v2
```

e.g.

```
az vm resize --resource-group adams-linux-play --name adams-ubuntu-001 --size Standard_B2S
```

Standard_E4s_v3 (4 vcpus, 32 GB memory) approx $300/month
Standard_B2S (2 vcpus, 4 GB memory) approx $30/month