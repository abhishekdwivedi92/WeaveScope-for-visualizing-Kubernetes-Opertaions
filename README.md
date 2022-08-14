# WeaveScope-for-visualizing-Kubernetes-Opertaions

For setting up WeaveScope for visualizing Kubernetes Pods, Services, Containers & Hosts we have to follow steps as mentioned bellow:

#### Pre-requisite
1. [Docker](https://docs.docker.com/desktop/install/linux-install/)
2. [Kubectl](https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html)
3. [AWS EKS Cluster](https://github.com/knoldus/Cloudformation-Template-for-AWS-EKS)
4. [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

kubectl create clusterrolebinding "cluster-admin-$(whoami)" --clusterrole=cluster-admin --user=<AWS username>
