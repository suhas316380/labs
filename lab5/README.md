Lab 5 EKS Windows Troubleshooting
---

Learning Objectives
===
* Intermediate/Advanced Kubernetes troubleshooting
* Node access through aws-auth ConfigMap
* EKS Windows requirements and functionality

Tasks
===
1. Scale any existing nodegroups to 0 so that you have 0 worker nodes in your cluster.
2. Deploy linux worker nodes to your cluster using the provided CloudFormation template `amazon-eks-nodegroup.yaml`. Do not use template provided in the AWS Documentation. Be sure to modify your aws-auth ConfigMap and ensure your worker node joins successfully. 
3. Windows pods have a pre-req before they can be successfully deployed. Follow the directions [here](https://docs.aws.amazon.com/eks/latest/userguide/windows-support.html#enable-windows-support) to install them.
4. Deploy your Windows nodes using the provided CloudFormation template `amazon-eks-windows-nodegroup.yaml`. Do not use template provided in the AWS Documentation. Be sure to modify your aws-auth ConfigMap and ensure your worker node joins successfully. 
5. Deploy `windows.yaml` and observe windows pod state. 
6. Troubleshoot and resolve Windows pod issue.

