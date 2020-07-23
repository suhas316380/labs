Lab 6 Isolated Cluster
===

Learning Objectives
---
* VPC Requirements for EKS cluster

Tasks
---
1. Create two additional subnets in different AZs in the VPC created by eksctl from `lab1`. The route table on these subnets should not have a NAT GW/IGW or any kind of internet access.
2. Using the console, create an EKS using these two new subnets.
3. Launch worker nodes in these subnets with the example linux CloudFormation template so that they will join the EKS cluster. (Hint: Having a bastion host so you can SSH into these isolated nodes may prove helpful in troubleshooting)
4. Use Public and Private endpoint for the cluster
