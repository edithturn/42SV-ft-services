# ft-services
Ft_services will introduce you to Kubernetes. You will discover cluster management and deployment with Kubernetes. You will virtualize a network and do "clustering".

## Set up a multi-service cluster.


### General
- [x] Each service run in a dedicated container
- [ ] Each Each container must bear the same name as the service
- [ ] Container have to build using Alpine Linux
- [ ] Create the Dockerfile to each service
- [ ] Kubernetes web dashboard
- [ ] Load Balancer
- [ ] Load Balancer with a single IP

### WordPress
- [ ] WordPress website listening on port 5050
- [ ] WordPress working with MySql database
- [ ] WordPress website with several userrs and an administrator
- [ ] WordPress needs its own nginx server.
- [ ] LoadBalancer able to redirect directly to this service

### phpMyAdmin
- [ ] phpMyAdmin, listening on port 5000
- [ ] phpMyAdmin linked with MySQL database
- [ ] phpMyAdmin needs its own nginx server.
- [ ] LoadBalancer able to redirect directly to this service

### Nginx
- [ ] nginx server listening on port 80 and 443
- [ ] Port 80 should be in http and should be a systematic redirection of type 301 to 443, which be in https
- [ ] The displayed does not matter as long as it is not an http error
- [ ] This container allows access to a /wordpress route that mkes a redirecto 307 to IP:WPPORT
- [ ]  This container allows access to /phpmyadmin with a reverse proxy to IP:PMAPORT

### Ftps, Graphana, InclusDB
- [ ]  A FTPS server listening on port 21
- [ ]  A Grafana platform, listening on port 3000, linked with InfluxDB database.
- [ ]  Grafana monitoring all the containers
- [ ]  In Grafana, create a dashboard per service.
- [ ]  InfluxDB and Grafana in two distincts containers
- [ ]  If crash or stop one of the two databases containers, make sure the date persist
- [ ]  Access the Nginx container by logging into SSH
- [ ]  Restar all the containers in case of a crashed or stoped
- [ ]  All the redirection toward a service is done using a load balancer.
- [ ]  FTPS, Grafana, WordPress, PhpMyAdmin and nginx's kind must be "LoadBalancer"
- [ ]  InfluxDB and MySql's kind must be "ClusterIP".
- [ ]   None of them can be of kind "NodePort"


## Kubernetes Dashboard


## Concepts


**MetalLB**: 
**InfluxDB**


## Installation and configuration of your environment Minikube

### 42 Virtual Machine
Download 42 VIrtual Machine:
https://mega.nz/file/x7gkVRKQ#qyIgYF0ZVRgrt8eyYx6kxV80FCopaH5ox3W6koBw8Ho


### Local Environment Minikube - Linux Ubuntu20.0

**Docker Installation**

```bash
sudo apt-get update
sdo apt-get instll apt-transpor-htto ca-certificates curl software=propetyies-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
udo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
sudo apt update
sudo apt install docker-ce
docker hello-world

```
**Install Required Packages**
```bash
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install curl
sudo apt-get install apt-transport-https
```
**Install VirtualBox Hypervisor**
```bash
sudo apt install virtualbox virtualbox-ext-pack
```

**Install Minikube**
```python
wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo cp minikube-linux-amd64 /usr/local/bin/minikube
sudo chmod 755 /usr/local/bin/minikube
minikube version
```

**Install Kubectl**
```bash
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
kubectl version -o json
```

**Start Minikube**
```bash
minikube start
```
**managing Kuberentes with Minikube**
```bash
kubectl config view
kubectl cluster-info
kubectl get nodes
kubectl get pod
minikube ssh
exit
minikube stop
minikube status
minikube delete
minikube addons list


```

**Testing Minikube installation**



SOurces:

Prepare Environment : https://phoenixnap.com/kb/install-minikube-on-ubuntu


### FT_SERVICES pdf  new curriculum
[Download from HERE](https://drive.google.com/file/d/1x3_JV38GSzlpNDzs7W7Ewuf_xgIxw3LT/view?usp=sharing)
 

