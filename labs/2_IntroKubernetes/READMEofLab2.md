# Introduction to Kubernetes

## LOs:

- Use the kubectl CLI
- Create a Kubernetes Pod
- Create a Kubernetes Deployment
- Create a ReplicaSet that maintains a set number of replicas
- Witness Kubernetes load balancing in action

## Steps for Kubernetes

1. To build an image 
    docker build . -t myimage:v1 

2. To get cluster information 
    kubectl config get-clusters

3. To view context information
    kubectl config get-contexts

4. To list all the pods
    kubectl get pods

5. To run image (from step 1) as a container (creates a pod)
    kubectl run hello-world --image myimage 

6. To describe pod 
    kubectl describe pod hello-world 

7. To create a pod imperatively
    kubectl create -f hello-world-create.yaml

8. To apply commands imperatively
    kubectl apply -f hello-world-apply.yaml

9. To load-balance 
    kubectl expose deployment/hello-world
    kubectl proxy