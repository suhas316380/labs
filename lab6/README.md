Lab 6 Isolated Cluster
===

Learning Objectives
---
* VPC Requirements for EKS cluster

Tasks
---
1. Create two additional subnets in different AZs in the VPC created by eksctl from `lab1`. The route table on these subnets should not have a NAT GW/IGW or any kind of internet access.
2. Create an EKS cluster using these two new subnets: `subnet-123,subnet-456`
3. Once the cluster is created, change the endpoint access from public to "private and public"
4. Launch worker nodes in these subnets with the example linux CloudFormation template so that they will join the EKS cluster. (Hint: Having a bastion host so you can SSH into these isolated nodes may prove helpful in troubleshooting)

