# Kubernetes
## Why Kubernetes
### Kubernetes Vs Docker 
### Docker 

![image](https://user-images.githubusercontent.com/130353146/236672871-9af0967b-b8b4-4a2f-a3a5-bcfd3190ce3f.png)

in Docker 
- Containers on node1 cannot communicate with node2 
- all the Containers on a node must share the host IP space and must coordinate which ports they use on that node 
- If a container must be replaced it will require new IP address, and any hard coded IP address will break

We can leverage this issues in Kubernetes 
### Kubernetes

![image](https://user-images.githubusercontent.com/130353146/236672897-025e476d-3b42-4f7f-9e86-de9d32cefbc7.png)

Kubernetes has 
- A master node and worker nodes 
- Kubernetes deploys pods (smallest unit in the Kubernetes is the pod). The pod holds the IPaddress so all the containers in the pod has same IPaddress
- all the pods in a cluster has unique IPs in the IP space 
- all containers can communicate with other containers
- All the node can communicate with all the other containers in a cluster 
- The IPaddresses are given by Network overlay and it helps in IP management
- Everything gets stored in etcd which is a key value store for the cluster so all of the objects have a metadata in that.

## Master and Nodes 
### Master 

![image](https://user-images.githubusercontent.com/130353146/236675366-e62f79b3-2c6e-4240-a1bf-28547aa11e84.png)

#### Etcd 
It is a key value store for the cluster when an object is created the object is stored here 

etcd acts as the reference for the clsuter state.if the clsuter differs from what is indicated the cluster is changed as per match.

#### API Server
It is a front end for Kubernetes control plane.All API calls are sent to this server and the server send commands to other services.

#### Scheduler
watches the nodes and determines when a pod needs to be deployed

when a new pod is created the Scheduler determines which node the pod will be run on. 
this decision is based on many factors including hardware, workloads, affinity

#### Controller Manager 
it operates the cluster controllers

**Node controller**

Responsible for noticing and responding when nodes go down

**Replication controller**

Responsible for manitaining the correct number of pods for every replication controller object in the system

**Endpoints controller**

Populates the Endpoints object (i.e, joins services and pods)

**Service Account & Token controller**

creates default accounts and API access tokens for new namespaces

### Node
![image](https://user-images.githubusercontent.com/130353146/236675770-1701f54b-d12e-4bc9-888f-96332cc28b73.png)
#### Proxy 
this runs on the nodes and provides network connectivity for services on the nodes that connect to the pods. services must be defined via API in order to configure the proxy 
#### Kubelet
This is the primary node agent that runs on each node. It uses PodSpec, a provided object that describes a pod to monitor the pods on its node.

the Kubelet checks the state if its pods and ensures that they match the spec.

#### container runtime
this is a container manager.it can be any container runtime that is complaint with open conainer intiative (such as docker). when kubernetes needs to instantiate a container inside of a pod, it interfaces with the container runtime to build the correct type of container.
