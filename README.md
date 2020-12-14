# ft-services
Ft_services will introduce you to Kubernetes. You will discover cluster management and deployment with Kubernetes. You will virtualize a network and do "clustering".



## Check List

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
