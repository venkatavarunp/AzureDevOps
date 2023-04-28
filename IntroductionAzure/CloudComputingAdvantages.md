# Cloud Computing
## Azure Managed Services
Managed services meant as managed solutions azure manages the servers so that we can focus on the code, data, solutions, etc.

Let us take an example of Azure SQL Database
For Azure SQL database Azure Manages 
- OS updates/Patching
- Backups
We manage 
- Compute and storage configuration
- loading and working with the data 
Different managed services handle different management responsibilities for different services.
## Different Managed services in azure
### Container/Kubernetes Services
Azure handles the container management infrastructure so that we can focus on containers.
### Artifical intelligence/Machine Learning
Enables application to automatically recognize patterns

we can use Pre trained services or build own custom model and we can let azure handle the custom model training for us. 
### Big Data 
Azure provides multiple services for different workflows
#### HDInsight
It is a managed suite of tools for Hadoop and spark workloads
#### Azure Synapse
It is a serverless fully managed service that allows to query absolutely massive amounts of data
#### Power BI 
A SaaS solution that provides dsashboards for taking the results of azure synapse queries and turning them into dsashboards to navigate.
### IoT Solutions 
the solutions for data collection process for IoT devices are 
- Ingestion, Storage, Analysis
- Intergrates with big data tools
## Cloud Advantages
the key Advantages of cloud Computing are 
- High Availabilty
- Fault Tolerance (Redundancy/Resiliency)
- Disaster Recovery
- Scalability
- Elasticity
- Business Agility

They can help in 
- Automatic, On-demand resources when needed
- Automatic failover in case of error
- Seperation of storage and compute

### High Availabilty
Maintaining acceptable continous performance despite temporary load fluctuations or failure in services, hardware or data centers.

**Data Center Redundancies**
- Power
- Cool 
- Networking

**Availabilty Zone Redundancies**
- 1 or more data centers

**Region Redundancies**
- Multiple availabilty zones
### Fault Tolerance
A system's ability to continue operating properly when one or more of ots components fails.

we have two ways to be fault tolerant

**Proactive**
- regular backup of data/apps/resources 
- deploy to multiple availabilty zones or regions
- load balance across multiple zones or regions 
- monitor health of data/apps/resources.

**Reactive**
- restire data/apps/resources to different availabilty zones or regions 
- deploy to different availabilty zones or regions 
### Diaster Recovery
a system's ability to back up and restore data/apps/resources when needed.

we can use azure to restore 
- On-premises to on-promises
- on-premises to azure 
- other cloud to azure
- azure to azure
### Scalability
The ability to increase the instance count or size of exisitng resources
#### Scaling Out
- increase instance count of existing resources
- Non-disruptive
#### Scaling Up 
- increase instance size of exisitng resources
- disruptive
### Elasticity
The ability to increase or decrease the instance count or size of existing resources based on fluctuations in traffic or load, or in resource workload.
- ability to scale in both directions
- can be manual or automatic 
- based on changes in load or workload 
- pay as you go
### Business Agility 
An organisation ability to rapidly adapt to market and environmental changes in prouctive and cost-effective ways and take advantage of availabile resources to meet customer demands.

![image](https://user-images.githubusercontent.com/130353146/235102725-3b0e212a-40aa-4917-8492-ef5873e6a1a5.png)
