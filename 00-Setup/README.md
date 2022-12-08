# In the following demo will be setting up 3 Node Kubernetes Cluster ( 1 Master & 2 Workers ) 

## For this demo will be required to have following tools installed. 
1.	Virtual Box
2.	Vagrant 
3.	Cmder / Git Bash 

## First clone this repository on your windows machine.

```
git clone https://github.com/amitvashisttech/devops-ericsson-08-Dec-2022.git
``` 

## Now provision three virtual machines with following commands:

```
cd devops-ericsson-08-Dec-2022/00-Setup
vagrant.exe up


vagrant.exe status
Current machine states:

master                    running (virtualbox)
worker1                   running (virtualbox)
worker2                   running (virtualbox)
```

## Let's login to the instance 
```
vagrant.exe ssh <nodename> 
```


## Let's Stop / shutdown to the instance 
```
vagrant.exe halt <nodename> 
```


## To Destroy the instance 
```
vagrant.exe destroy <nodename> 
```


