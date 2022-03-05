# CLIENT-SERVER ARCHITECTURE WITH MYSQL
Created the 2 EC2 instances - mysql server & mysql client => Successful

![2022-03-05 14_17_36-Window](https://user-images.githubusercontent.com/97810379/156884746-a34c66cf-fbe4-4222-a61c-b14db9c742ed.jpg)

## Install mysql server on the server EC2 instance
sudo apt-get update

sudo apt-get upgrade

sudo apt install mysql-server

![2022-03-05 14_35_41-](https://user-images.githubusercontent.com/97810379/156886189-0da43340-7847-46fc-906a-ea42c5c53b6b.jpg)

sudo mysql_secure_installation -> To set the password and disable all the defaults

sudo mysql -> To enter the sqlserver

mysql> exit

## Install mysql client on the client EC2 instance
sudo apt-get update

sudo apt-get upgrade

sudo apt install mysql-client

![2022-03-05 14_39_37-ubuntu@ip-172-31-87-51_ ~](https://user-images.githubusercontent.com/97810379/156886211-aedc05c5-588c-40cc-b25e-b7979806cefb.jpg)

## Security Changes and Configuration Settings on the Server
Opened port 3306 for the client private ip address to enable the client to connect to the server. It was not opened to all for added security.

![2022-03-05 14_49_10-EC2 Management Console](https://user-images.githubusercontent.com/97810379/156886339-5bac3b23-de14-4c0d-8fdc-21a113c01557.jpg)

Configured MySQL server to allow connections from remote hosts by editing the mysqld.cnf file

sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf

Replace 127.0.0.1 with 0.0.0.0 and save.

![2022-03-05 15_01_49-ubuntu@ip-172-31-84-163_ ~](https://user-images.githubusercontent.com/97810379/156886645-279c565b-10ca-4cb7-bbb6-c6660605284f.jpg)

Restarted the mysql service ->- sudo systemctl restart mysql

Created the remote user 'username'@'client-ip-address'

mysql>  CREATE USER 'TestUser'@'172.31.87.51' IDENTIFIED BY 'password';

![2022-03-05 16_29_05-MINGW64__c_Users_1_Downloads_DevOps](https://user-images.githubusercontent.com/97810379/156889905-cf593c7c-1b85-4916-afdb-d0b4037caf21.jpg)

Grant all permissions to enable access for the remote user (client)

mysql>  GRANT ALL ON fooDatabase.* TO 'TestUser'@'172.31.87.51';

![2022-03-05 16_29_56-MINGW64__c_Users_1_Downloads_DevOps](https://user-images.githubusercontent.com/97810379/156889916-ed6f63a7-ea2f-4591-abcc-bb654bcc230f.jpg)

## Connecting to the Server from the Client
mysql -u username -h mysql_server_ip -p

Enter Password: 

Connection successful

![2022-03-05 16_37_33-ubuntu@ip-172-31-87-51_ ~](https://user-images.githubusercontent.com/97810379/156890107-8af94ae0-5928-4b48-9e1f-ef7d6d7b0ecf.jpg)

Test 
