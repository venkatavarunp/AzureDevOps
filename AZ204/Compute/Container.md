# Containers 
can be created using azure cli and powershell

azure cli example 
```
az container create \
    --resource-group examplerg \
    --name examplecontainer \
    --image <path or url> \
    --dns-name-label exaamplecontainer \
    --ports 80
```
powershell example 
```
New-AzContainerGroup 
    -ResourceGroupName examplerg \
    -Name examplecontainer \
    -Image <path or url> \
    -DnsNameLabel exaamplecontainer \
    -OsType Windows
```
## Container Instance Management
Azure has two container instance management
### Container Group 
if a container needs additional resources such as storage account,vnet,etc as a dependency these all make up as a group as container needs them to function properly
### Container Operation

