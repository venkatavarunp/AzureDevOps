# Introduction to Azure DevOps
## Azure DevOps Structure
![image](https://user-images.githubusercontent.com/130353146/235134963-6cea2618-6fcc-477e-95b7-d21d4d40e2b3.png)

Anyone with microsoft account can create a devops environment that is called as organisation

we can have multiple projects in an orgainsation but one team project resources cannot be shared with other team project so it always preferred to create a single team project and have multiple teams for different tools 

![image](https://user-images.githubusercontent.com/130353146/235135162-9c6b8295-1b97-4e7e-b10b-acd22e6936f2.png)

## Team Project Options
We need to specify options to create a team project 
- Private Project or Public Project 
- Work Item Process

![image](https://user-images.githubusercontent.com/130353146/235136195-422d1297-7cdb-4cfe-9ad5-20acc347f2a3.png)

The work item process decides which work item types are available in the product and how they can be used

These are four work item process available
- Agile Process 
- Scrum Process 
- CMMI Process 
- Basic Process

### Agile Process 
Default process for all new team projects

In this work item process are 
- Epic
- Feature 
- User Story 
- Task

![image](https://user-images.githubusercontent.com/130353146/235139650-c5675ca3-d38f-4a33-8894-bb7cd03b06b7.png)

User Stories are the items that we normally move from a product backlog to sprint backlog or iteration.

Within this iteration we can refine the user stories with concrete tasks to be performed

User stories have a state that describes whether they are new, active, that's being worked on, resolved, closed or Removed.

User Stories can be organised below features which can optionally, be organised below Epics

Epics and Features are only used on a product backlog to perform portfolio management and are not used within an iteration

Within User story we can enable the work item type of a bug.It is handy if we want a different trait between bugs and regular user stories on our backlog

if we want to differentiate between bug and regular user stories from your backlog just as a story a book can be divided into a number of concrete tasks and be placed in a Sprint or iteration 

### Scrum Process
The difference of Scrum from Agile process is the PBI (product backlog item) and the states that the story can be in also different. The PBI can be New, Approved, Committed, Done or Removed.

![image](https://user-images.githubusercontent.com/130353146/235140596-05562379-3fea-4d85-b8d7-347a0b5e3977.png)

### CMMI Process 
CMMI is less known and more formal process for change management.The 3rd level of work item is a requirement.

Requirements can be proposed, Active, resolved and closed.

Bugs are also available to tracking defects.

![image](https://user-images.githubusercontent.com/130353146/235141141-b53d33ef-461c-43af-9b95-9f470a1bd680.png)

### Basic Process 
A new, more lightweight, basic process to get started and suitable for small teams.

Work items supports the To Do, DOing and done states 

![image](https://user-images.githubusercontent.com/130353146/235141555-069b414f-c889-4173-8818-a2b22153f436.png)

## Azure DevOps Licensing
These costs come in two dimensions
- User Licensing 
- Other Consumables
For users there are three types of licenses
### Basic Plans
can access all service offerings, except test plans

Every Visual Studio professional subscriber gets a license like this for free 

First five users are free holders of Visual Studio professional do not count towards this five.
### Basic + Test Plans
Users with this type of licensecan also create and manage test plans

Every Visual Studio enterprise subscriber get this type of license for free 
### Stakeholder
They are limited to what they can do with the product.

They do have access to Azure Boards for work management

They do not have access to source control via azure repo

In pipelines they can view bills and release and approve deployments to environments

They have no access to the azure test plans and azure artifacts

They can view dashboards but can not create or edit them

Stakeholder licenses are free 
### Other Consumables
| Private Projects | Public Projects |
|:--|:--|
| 1 concurrent CI/CD hosted jobs with 1800 minutes per month | 10 concurrent CI/CD hosted jobs with unlimited minutes included |
| 1 concurrent CI/CD self hosted job with unlimited minutes | Free access to boards, repositories and pipelines for anonymous users|
| 2GB of storage for azure artifacts | N/A |
