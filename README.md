## Prerequisites
Prerequisites
The following prerequisites are required for a successful and properly secured use of Helm.

A Kubernetes cluster
Deciding what security configurations to apply to your installation, if any
Installing and configuring Helm.
Install Kubernetes or have access to a cluster
You must have Kubernetes installed. For the latest release of Helm, we recommend the latest stable release of Kubernetes, which in most cases is the second-latest minor release.
You should also have a local configured copy of kubectl.
See the Helm Version Support Policy for the maximum version skew supported between Helm and Kubernetes.

Install Helm
Download a binary release of the Helm client. You can use tools like homebrew, or look at the official releases page.

For more details, or for other options, see the installation guide.

## Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL
## Database
Here,we used Mysql DB 
MSQL DB Installation Steps for Linux ubuntu 14.04:
- $ sudo apt-get update
- $ sudo apt-get install mysql-server

Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < accountsdb.sql

## Commands to Execute
kops create cluster --name=kube
kops update cluster --name kube
kubectl file
cat ~/.kube/config

start the cluster
kops validate cluster --state=s3://vprofile-anil-kops-state

kubectl create namespace dev


https://helm.sh/docs/intro/quickstart/
https://helm.sh/docs/intro/install/

Download your desired version
Unpack it (tar -zxvf helm-v3.0.0-linux-amd64.tar.gz)
Find the helm binary in the unpacked directory, and move it to its desired destination (mv linux-amd64/helm /usr/local/bin/helm)

https://github.com/anlkmr/cicd-kube-docker/tree/master
go in to emagia folder and check the files existing.

kubectl create namespace dev

helm install --namespace dev emagia-stack helm/emagiacharts --set appimage=anlkmr/restdocker:v1

helm list --namespace dev

kubectl get all --namespace dev

use dns to hit

helm delete emagia-stack --namespace dev

kops delete cluster --name kube

