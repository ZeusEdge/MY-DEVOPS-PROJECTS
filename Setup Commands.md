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

## COMMAND TO RENAME A FILE
mv 'old filename' 'new filename'

## COMMAND TO LOGIN TO MYSQL WITH CUSTOM USER CREDENTIALS
mysql -u 'custom_user' -p

## USER & GROUP MANAGEMENT
Add a new user =>= _sudo useradd -m "username"_

Add a new group =>= _sudo groupadd "groupname"_

Assign user to a group =>= _usermod -a -G "groupname" "username"_ -> This ensures the user is still assigned to previous groups

_usermod -a -g "group-name" "username"_ -> This removes the user from all previously added groups and assigns to the specified group

Delete a user =>= _sudo userdel "username"_

Delete a group =>= _sudo groupdel "groupname"

Adding a user to the sudoers file =>= _usermod -a -G sudo "username"_

Adding executable permissions to a file =>= _chmod +x "filename"_
