## COMMAND TO CONNECT TO THE EC2 INSTANCE
Change directory to the Filepath to the location of the pem file downloaded when setting up the instance.

ssh -i Your-private-key.pem ubuntu@EC2-Public-IP-address

## COMMAND TO SET UP MYSQL
sudo apt install mysql-server

sudo mysql_secure_installation

sudo mysql

mysql> exit

## COMMAND TO SET UP PHP
sudo apt install php-fpm php-mysql
