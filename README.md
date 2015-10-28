# AzureVMSetup


Accessing your virtual machine remotely
=========
* Please download putty from: http://www.putty.org/ 
* To connect to your virtual machine use the DNS assigned to the VM. e.g. foo.cloudapp.net
* If you are not familiar with Shell/Bash, please check out some tutorials here:
  * http://www.freeos.com/guides/lsst/
  * https://en.wikipedia.org/wiki/Unix_shell
 

Setting up an Azure Virtual Machine
===========
General configuration of packages for LAMP stack (https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu):

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

To install GitHub (https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04):
```
sudo apt-get update
sudo apt-get install git
```


Azure Portal Configuration - Ports (ENDPOINTS)
===========

Navigate to your Azure management portal (https://manage.windowsazure.com/):
* Virtual machines -- click on your VM name
* ENDPOINTs - click this
* Add the following ports: 80, 443, 27015, 27017, 3000, 3006, 9000
