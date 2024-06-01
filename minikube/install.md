  ## installing process-->
  -->install kubectl from browser
  --> install minikube from the browser--->

# apply the command
      minikube start
  ----> OR
      minikube start --memory=4096 --driver=hyperkit

# check
       kubectl get nodes
  
# creating pod --> from browser copy the things of pod.yaml
 -----> apply command
       kubectl create -f pod.yaml

# to check pods
       kubectl get pods
  
 ---> to check entire details
       kubectl get pods -o wide

 # login to kubernetes cluster
       minikube ssh

 ---> after the login
      curl --> ip adress


 # checking errors and debug
       kubectl describe pod (name of the pod)

OR
       kubectl logs (name of the pod)
  
