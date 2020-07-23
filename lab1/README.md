Lab 1 Cluster Troubleshooting
===

Learning Objectives
---
* Basic Kubernetes troubleshooting
* DNS logging/troubleshooting
* Node access through aws-auth ConfigMap

Tasks
---
1. Create an EKS cluster using eksctl with the following command `eksctl create cluster --name training --nodes 0 --ssh-public-key <your key name>`
2. Once the cluster is created, scale the nodegroup to 1 node. Ensure that it is running and joined the cluster.
3. Modify the nodeName value in `node1.yaml` and deploy it to the EKS cluster. 
4. Launch another nodegroup containing 1 node into the cluster using the AWS provided [CloudFormation Template](ttps://docs.aws.amazon.com/eks/latest/userguide/launch-workers.html). Use self-managed nodes.
5. After the node has joined the cluster, deploy `node2.yaml` to the new node.
6. Create the namespace `nginx` in your cluster. Inspect `nginx.yaml` and then deploy it to your cluster. 
7. Exec into the node1 pod and node2 pod in separate terminals. Curl both the nginx service, the cluster IP, and the pods directly. Note any differences.
8. Enable the `log` plugin in CoreDNS. Observe the difference in logs when making DNS queries to the `nginx` service.
9. Ensure that both nodes are able to successfully curl the nginx service through DNS, ClusterIP, and the pods directly.
