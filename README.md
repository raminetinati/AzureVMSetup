# AzureVMSetup
Setting up an Azure Virtual Machine
===========

General configuration of packages for LAMP STACK:

```
sudo apt-get update
sudo apt-get install apache2
sudo apt-get install mysql-server libapache2-mod-auth-mysql php5-mysql
```

To install MongoDB (Please check https://docs.mongodb.org/manual/tutorial/install-mongodb-on-ubuntu/ for more details):
```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
sudo apt-get update
sudo apt-get install -y mongodb-org
```
