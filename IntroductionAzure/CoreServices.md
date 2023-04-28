# Core Services
## Virtual Machines (Compute)
Azure VM is as virtual computer same as a physical computer at azure cloud and can be accessed by internet

VMs are simulations of physical computers and all azure VMs are servers, Linux or Windows

VMs include network cards, disks, processors/RAM(VM) and an OS and are the highest cost center of most Azure Deployments.


VM's are known as `IaaS` Service.

**Azure's Responsibility**
- Physical Hardware and networking
- Base OS image
- Hypervisor (Virtualisation) Management
**User's Responsibility**
- Updating/Patching OS and installed software
- OS access and management
- software installation

VM's provides more flexibility when compared to Mangaged services.

**Advantages of azure VM when compared to on Premise**

### Availability Set 
availability set is a replication or automatic copy of one virtual Machine to another in a different availability zone.
### Scale set
A scale set is often paired with a load balancer in which we can have multiple copies of VMs which helps us to scale up or down applications based on user demand.

## Networking 
Networking includes virtual networks, load balancers, DNS,  ExpressRoute, Traffic Manager, VPN gateway, App gateway.

### Virtual Network (VNet) 
is the basic building block of networking for all azure communications.

It can provide both `private` and `public` network communication among azure resources.

Virtual format of networking concepts is referred as `Software Defined Networking (SDN)`

Using SDN we can enable the combination of different types of publi access or choose to keep different types of communication private or internal only.

VNet in azure very closely mimic the setup, configuration and architecture of networks in op-premise locations 

Each Subscription and region can have many virtual network

Those networks can be combined and structured in many different ways to achieve a comprehensive and complex network design

**On Azure a VNet can exist only in a single region at a time although other options do exist to connect seperate virtual network across regions**

**Private Network**

![image](https://user-images.githubusercontent.com/130353146/235067131-c5671232-a9f6-4ca5-9a1f-66e0b73cff66.png)

Router helps to deignate the private network and communications among those devices on that private network are not visible to outside world

Router also allows the devices inside private network to communicate with the public internet

private networks use a private or internal ip addresses to communicate in private network.
The internal IP addresses are not visible to outside world and outside world won't be able to see the specific communications

**A VM on azure can have both an internal and external addresses depending on the level of public access that we want to give to that machine.**

### Subnets
Segment multiple resources for precise Organisation.
### Peering/VPN/Express Rooute
Connect to other azure VNets across regions, on-Premise networks, or other cloud networks
### Network Security Groups/Firewall
Control access to VNet resource by network protocol ,port, or source locations.

## Storage
Azure's all purpose Storage solution for multiple data Storage scenarios and these are massively scalable and is a managed infrastructure.


![image](https://user-images.githubusercontent.com/130353146/235069798-8882b55b-c064-42b7-8ce8-13b52c7583dc.png)

All storage types (Blobs, Disks, Queues, etc)are organised into `Storage Accounts`

### Blob (Binary Large Object)
Object storage is often referred to as unstructured data (images, videos, scripts, any type of file)
### File 
Same as Blob but acts as a remote server that is available on a cloud vendor

Network file share in the cloud.
### Disks
Disks host virtuak hard drives for virtual Machines

When we create a VM defaultly the Disk is under managed storage account.
### Queues
It is a Asynchronous messaging system between apps and services.
### Tables
Tables provide NoSQL database storage inside of a service account, Microsoft gradually transitioning the tables sub service type inside of storage accounts and added storage accounts into  seperate managed cosmos DB database service.
## Databases and Analytics
### DataBases
Databases and webapps comes as managed services and core services.

Databases are made up of structures data arranged in tables and rows

Mangaged Database services are `PaaS`

Azure offers multiple options with different use cases/levels of Management for managed Database services
- SQL vs NoSQL 
- Fully Managed vs Provisioned Infrastructure( we can set the compute specs/storage space vs azure dynamically does it for us)
- Single region vs multiple regions
- open source vs proprietary
### Analytics
Analyzing data for insights and the data is mostly massive ( Terabytes to petabytes).
#### Azure Synapse
It is service used for quering and visualising massive amounts of data
#### Azure Data Lake
It is seperate service used essentially as a large dumping ground for absoluely massive amounts of data to query.

## App Service and Serverless Compute 
### App Service
App service leverages the challenges of hosting applications on VMs that include 
- OS updates and Patching
- compute and storage management
- scaling via VM scale sets 
Overall these increases the Responsibility so we use azure app service which takes care of all above.
### Serverless Compute 
Serverless compute uses a server or VM to power it and servers are taken care by the vendor.
