Lab 2 Cluster Access with Roles
===

Learning Objectives
---
* Basic Kubernetes troubleshooting
* User/Role access to EKS cluster
* IAM

Tasks
---
1. Create a role named `EKS-Master` with the admin access policy attached. Ensure the IAM identity you have configured your awscli with is able to assume this role.
2. Give this role `system:masters` permission to the cluster by modifying the `aws-auth` ConfigMap.
3. Access the cluster via the new role.
