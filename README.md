# WeaveScope-for-visualizing-Kubernetes-Opertaions

For setting up WeaveScope for visualizing Kubernetes Pods, Services, Containers & Hosts we have to follow steps as mentioned bellow:

#### Pre-requisite
1. [Docker](https://docs.docker.com/desktop/install/linux-install/)
2. [Kubectl](https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html)
3. [AWS EKS Cluster](https://github.com/knoldus/Cloudformation-Template-for-AWS-EKS)
4. [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

_kubectl create clusterrolebinding "cluster-admin-$(whoami)" --clusterrole=cluster-admin --user="<AWS username>"_
  
#### Clone the repo
  
#### Installing WeaveScope
  
  _kubectl appy -f weave.yaml_
  
  This will deploy weave scope in cluster and launches a probe onto every node as well as a single Scope app. Once launched, Scope doesn’t require any other configuration.
  
  Allowable parameters for the launcher URL:
  
  _v - Weave Scope version or tag, e.g. latest current release is the default
k8s-service-type - Kubernetes service type (for running Scope in Standalone mode), can be either LoadBalancer or NodePort, by default this is unspecified (only internal access)_
 
 #### Open Scope in Your Browser
  
  _kubectl port-forward -n weave "$(kubectl get -n weave pod --selector=weave-scope-component=app -o jsonpath='{.items..metadata.name}')" 8080_
  
  Now get ready to access via http://localhost:8080
  
  ![alt text](https://www.linkpicture.com/q/weave.jpg)

