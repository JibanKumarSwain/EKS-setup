# EKS-setup


## How to Setup the AWS EKS ?

## We need to install AWS kubectl 

## Install kubectl binary with curl on Linux          
               
 curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
          
 ## Install kubectl

 sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

 ## Note: If you do not have root access on the target system, you can still install kubectl to the ~/.local/bin directory:
   
 chmod +x kubectl 
     
mkdir -p ~/.local/bin      

mv ./kubectl ~/.local/bin/kubectl     


 ## Test to ensure the version you installed is up-to-date:

kubectl version --client
 


##  Setup EKS Cluster
 eksctl create cluster --name "cluser name" --region "region name" --node-type "which type node you need" --nodes-min "how much you need min" --nodes-max "how  much you need max"



  With all documents link = https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
