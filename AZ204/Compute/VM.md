# Virtual Machines 
VMs are simply virtualized servers running on azure hardware

Part of a IaaS offering and can be scalable and flexible in terms of compute and storage.

VM offering ranges from small,test optimized servers to massive, GPU bearing machine learninig systems.

In VM we can use windows or linux based servers, deploy pre-configured servers for databases,etc. we can  even use our own image.
## Deployment
### Deploying with PowerShell
the deployment of VMs will be done using PowerShell by `Az.Compute` module

- `New-` for deploying new systems or scale sets from scratch
- `Get-` to gather information and even plug returns into variables
- `Start-AzVM` and `Stop-AzVM` commands to power up and power down a VM (`Stop-AzVM` doesn't deallocate the VM)

[More PowerShell Commands](https://learn.microsoft.com/en-us/previous-versions/azure/virtual-machines/windows/tutorial-govern-resources)

### Deploying with Azure CLI
`az vm` command is used to run VM in azure 

`Command Groups` are key to azure CLI
### Deploying ARM Templates
`ARM Templates` are pre-configured scripts that can be used to deploy single machines or whole environments.

These templates are in JSON and can be linked together to create single or multiple modularized templates.

These can be deployed using
- Azure Portal
- Azure CLI
- PowerShell
- REST API
- GitHub
- CloudShell
## Secure and Manage
### Security
Make sure the system is always available or keeping services running
- preventing the network attacks
- Identity management 
- encrypt the data in transfer and in storage 
### Managing 
- Patching the VMs (microsoft can help in streamlining it for us)
- updating the required services in VM regularly
- scale the VM as per requirement
#### System Availability 
- virtual machine scalesets can help in automatic scaling
- backing up the data 
## ARM Templates
ARM templates are preconfigured template files used to automate and standardize environment deployments.

written in JSON and can be single file or multiple modularized templates and can be deployed in many ways

Templates are divided into several JSON elements
```
{
    "$schema":"",
    "contentVersion":"1.0.0",
    "apiProfile":"",
    "parameters":{},
    "variables":{},
    "functions":[],
    "resources":[],
    "outputs":{}
}
```
of the above only three elements are mandatory to create a resource 
### Mandatory elements
#### $schema 
provides the ARM with version of the template 

the version depends on the editor and deployment process

additional versions include
- other IDEs
- subscription deployments
- management group deployments
- Tenant deployments

#### contentVersion
It is the versioning tool and is the version of the template and is user defined and can hold any value that can be understandable by version control system.

#### resources
defines the services that will be deployed or configured 

### Optional elements
#### apiProfile
helps to keep azure and any azure stack locations
#### parameters
used to store service parameters to be used during deployment
- useful for creating deployment constraints
- ensure consistency in objects to be deployed via default values and locations
#### variables
used to create and define variables for the template script 
#### functions
place for any expressions that need to be placed in the script 
#### outputs
returns the values from deployed resources or event details
