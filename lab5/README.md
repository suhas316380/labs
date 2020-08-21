Lab 5 - Nginx Ingress Controller
===

Learning Objectives
---
* Ingress
* Kubernetes Nginx Ingress Controller

Tasks
---
1. Create 2 deployments: nginx and httpd and expose the deployments via service:
  - `kubectl create deploy nginx-deployment --image nginx`
  - `kubectl expose deploy nginx-deployment --name nginx-service --port 80 --target-port 80`
  - `kubectl create deploy httpd-deployment --image httpd`
  - `kubectl expose deploy httpd-deployment --name httpd-service --port 80 --target-port 80`
2. Deploy [Kubernetes version of nginx ingress controller](https://kubernetes.github.io/ingress-nginx/deploy/#aws). 
3. In the document, public NLB is created by default. Change it to internal ELB (Classic LoadBalancer). Hint: These settings are controlled through Service annotations.
4. Create 2 Ingress resources - one for nginx-service and one for httpd-service. Use path based routing
5. Bonus challenge: Use host based routing:
  - Create a R53 Private Hosted Zone
  - Setup `externalDNS` to automatically set the Ingress Controller LoadBalancer DNS name as an Alias target for the R53 Domain name. 
  - Create Ingress resource and use Host Based Routing
  - Access your application from within the VPC - Eg: curl mydomain.example.com
