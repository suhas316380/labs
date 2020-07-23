Lab 4 EKS IRSA
===

Learning Objectives
---
* Ingress
* ALB Ingress Controller
* IRSA
* InitContainers and Shared volumes

Tasks
---
1. Deploy the ALB Ingress controller to your cluster. Ensure that it is using IRSA for its IAM permissions.
2. Create an S3 bucket and store a few images in this bucket. They will be used later in this exercise.
3. Create a role that has S3 read only permissions and then create a Kubernetes ServiceAccount that will use that IAM role.
4. Use the skeleton deployment `random-deployment-skeleton.yaml` file to create the deployment. The container `random-container` and initContainer `s3-downloader` should share a volume. This volume should be of type `emptyDir` and mount to the `/images` path in both containers. Deploy this to your cluster.
5. Create a Service for this deployment. The Service should expect traffic on port 80. The container is expecting traffic on port 8080.
6. Finally, create an Ingress and ensure that you are able to access the service through the ALB created by the ALB Ingress Controller.
