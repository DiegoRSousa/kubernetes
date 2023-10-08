# kubernetes
## Repositório do curso de kubernetes da Alura

### Kubernetes
Kubernetes is an open-source container orchestration platform designed to automate the deployment, scaling, and management of containerized apllications.

### Architecture

### Pod
Pod is the smallest deployable unit in Kubernetes, it's used to automate the deployment, scaling, and management of containerized applications.

### SVC
Services are abstractions for exposing applications running in one or more pods that provide fixed IP's for communication and provide a dns for one or more pods as well as being capable of load balancing.

#### Cluster IP
It is the default service and its visibility is cluster internal.
Provides a load-balanced IP address. One or more pods that match a label selector can forward traffic to the IP address.

#### NodePort
Extends the ClusterIP and its visibility is internal and external to the cluster.
This expose the service on each Node's IP at a static port.

#### LoadBalancer
Exposes the service externally using an external load balancer.

### ReplicaSets
Is a higher-level abstraction used to ensure that a specified number of identical pod replicas are running at all time. ReplicaSets are often used for achieving high avalilability, load balancing, and scaling applications within a Kubernetes cluster.

### Deployment
Is a ReplicaSet providing declarative update for pods and ReplicaSets

### Probes
The kubelet uses liveness probes to know when to restart a container, and uses readness probes to know when a container is ready to start accepting traffic.

### Horizontal Pod Autoscaler