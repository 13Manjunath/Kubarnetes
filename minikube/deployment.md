## list all the application and namespaces
     kubectl get all -and-  kubectl get all -A
     
# take the below exp and change as per the required information

    #copy the deploymeny filr and changeapiVersion: apps/v1
      kind: Deployment
      metadata:
        name: nginx-deployment
        labels:
          app: nginx
      spec:
        replicas: 1
        selector:
          matchLabels:
            app: nginx
        template:
          metadata:
            labels:
              app: nginx
          spec:
            containers:
            - name: nginx
              image: nginx:1.14.2
              ports:
              - containerPort: 80

## apply the command 

     kubectl apply -f deployment.yaml
## check for the apply 
it will create replica set 
     kubectl get deploy
## for replica set

     kubectl get rs
       
