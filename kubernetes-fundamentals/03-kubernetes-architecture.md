# Kubernetes Architecture

- **Nodes**
    - A node is a machine which could be physical or virtual where Kubernetes is installed
    - A node is where containers are launched and hosted by Kubernetes (previously known as minions)
    - You need to have more than one node for redundancy
    - A group of nodes is called a cluster
        - If one node fails, the application would be able to access other nodes
        - Multiple nodes help share load
    - Worker nodes have the container runtime
    - Worker nodes have </> kubelet agent installed to interact with the master node to provide health information of the worker node and carry out actions requested by the master on the worker nodes

    
    - Master node is another node configured as master 
        - Master node is controls the orchestration of containers on worker nodes
        - Master server has the kube-apiserver, which is what makes it a master
        - Information gathered is stored on a key-value store on the master (etcd)
        - Master has controller 
        - Master has scheduer


- **Components**
    - When Kubernetes is installed, the following is installed
        - API Server(</> kube-apiserver)
            - Master
                - Front end for Kubernetes
                - User management
                - CLIs all talk to API server to interact with the Kubernetes cluster
        - etcd
            - Master
                - Distributed key-value store
                - Used to store all data needed to manage the Kubernetes cluster
                - Implements logs within a cluster to ensure there are no conflicts between the masters
        - kubelet
            - Worker Node
                - Agent that runs on each node in the cluster
                - Responsible for making sure that the containers are running on nodes as expected
                - Used to deploy and manage applications on a Kubernetes cluster and to get cluster info
                    - `kubectl run hello-minikube` - Deploy an application to the cluster
                    - `kubectl cluster-info` - View information about the cluster
                    - `kubectl get nodes` - List all nodes that are part of the cluster
        - Container Runtime
            - Worker Node
                - Underlying software uded to run containers
                - Docker or other options
        - Controller
            - Master Node
                - Responsible for noticing and responding to nodes, containers, or endpoints go down
                - Controllers bring up new containers when containers go down
        - Scheduler
            - Master Node
                - Responsible for distributing work or containers across multiple nodes
                - Looks for newly created containers and assigns them to nodes






