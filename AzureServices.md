# Microsoft Azure Introduction
## Uses of Cloud Services
- Fault Tolerant
- High Availability
- Scalability 
- Elasticity
## Azure Organisation and Infrastructure
### What is Azure ?
- Microsoft's public cloud computing platform
- has over 200 individual products and Services
- Using Azure we can Build, run and manage applications on Microsoft's global Infrastructure
- Supplements or replaces existing On-Premises computing Services.
- Pay as you go pricing
### Azure Global Infrastructure
#### Regions
Group of datacenters in a single geographic location.
#### Availability Zone
One of several umique locations in a region.

These zones are made up of one or more individual data center builidings.

Availability zones helps to fault Tolerance  (resiliency) by offerinf the ability to replicate applications across multiple Availability zones in the same region.

![image](https://user-images.githubusercontent.com/130353146/233057269-7321de6d-4d1d-4e1d-9fe6-611436193a46.png)

#### Purpose of Regions and Availability zones
| Region| Availability Zone |
|:--|:-- |
| High Availability, Fault Tolerance| Fault Tolerance |
| Be closer to end users and helps during regional outages | Deploys resources across zones and Helps during single point of failure|

### Azure Services

![image](https://user-images.githubusercontent.com/130353146/233059414-2046d78a-a172-479d-a933-0adfa494881c.png)

### Azure Resource Manager
Regardless of the interaction method, all interaction methods go through a single portal referres to as `Azure Resource Manager`

Provides a centralised management layer and can be accessed by
- web portal
- Command line interface (CLI)
- Application Access 
`ARM` provides a centralised method of access control and authentication

### Resource Hierarchy and Organisation 

#### Azure Resource Hierarchy

![image](https://user-images.githubusercontent.com/130353146/233345076-95302625-6d51-49e4-a97a-e0e5e4890b43.png)

#### Azure Resource Hierarchy Fundamentals
- parent-child relationship
- Access/Policies granted to parent inherited by child levels
- Centralized management
- Parent can have multiple children -child can only have one parent
- Similiar to OS file structure
#### Azure resource Hierarchy components

![image](https://user-images.githubusercontent.com/130353146/233344683-0d03f837-9e07-4608-8bcd-e98f013433e0.png)

### Identity Access Management 
Identity Access Management helps in `who ? can do what ? on which resources ?`

![image](https://user-images.githubusercontent.com/130353146/233346392-4abe8117-e087-42e7-971d-5648318d8227.png)

#### Azure Active Directory (Azure AD)
An cloud based identity service (One per tenant)

![image](https://user-images.githubusercontent.com/130353146/233347686-8b0df640-4fdb-48fc-b024-6f11134504d8.png)

#### Azure Role-Based Access Control (Azure RBAC)
Controls access using roles

![image](https://user-images.githubusercontent.com/130353146/233348168-01053b1f-ea05-4cd3-ad76-62425e93fc9e.png)
#### Scope
![image](https://user-images.githubusercontent.com/130353146/233348672-0c2d542b-f1bd-4fab-9d99-4353a246cf98.png)
### Azure Monitor
Collects all logs and metrics from all azure sources
#### logs
Text based records of events
- Activity Logs (Who created the resource and when)
- OS logs (Why windows giving an error)
#### Metrics 
telemetry based performance data
- CPU Utilisaation
- Website latency

![image](https://user-images.githubusercontent.com/130353146/233379340-b45c8487-1fae-43c8-9a91-d941cdae1c1d.png)

Azure Monitor helps 
- Explore performance metrics in dashboard
- Troubleshoot windows system errors
- Automatically alert someone when somwthing goes wrong
- creates automated respones to events
## Core Services
### Virtual Machines (Compute)
