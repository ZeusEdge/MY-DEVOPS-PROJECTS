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

Opened port 3306 for the client private ip address to enable the client to connect to the server. It was not opened to all for added security.

![2022-03-05 14_49_10-EC2 Management Console](https://user-images.githubusercontent.com/97810379/156886339-5bac3b23-de14-4c0d-8fdc-21a113c01557.jpg)
