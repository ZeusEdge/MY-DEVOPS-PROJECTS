# WEB STACK IMPLEMENTATION (LEMP STACK)
## Most important SQL commands
SELECT - extracts data from a database

UPDATE - updates data in a database

DELETE - deletes data from a database

INSERT INTO - inserts new data into a database

CREATE DATABASE - creates a new database

ALTER DATABASE - modifies a database

CREATE TABLE - creates a new table

ALTER TABLE - modifies a table

DROP TABLE - deletes a table

CREATE INDEX - creates an index (search key)

DROP INDEX - deletes an index

Link to Major SQL commands - https://www.w3schools.com/sql/default.asp

Link to Major Nano commands - https://www.linuxandubuntu.com/home/nano-cli-text-editor-for-everyone-basic-tutorials

**0. Preparing Prerequisites**

Launched GitBash and connected to the EC2 instance created from Project1 => Successful

## 1. INSTALLING THE NGINX WEB SERVER
Tried installing NGINX on the previous EC2 instance => Successful

Confirmed the NGINX service is running => Server inactive (dead)

Attempted to access the server locally in the Ubuntu shell, run: curl http://localhost:80 => Output was from the Apache Server that was previously set up

Attempted to render the server on a web browser => Output was from the Apache Server that was previously set up

Removed NGINX from the EC2 instance by running "sudo apt remove --purge nginx" and "sudo apt autoremove" => Successful

Created a new instance => Successful

Tried connecting to the EC2 instance with GitBash => Unsuccessful, Error Message: permission denied (publickey gssapi-keyex gssapi-with-mic).aws

![Error connecting to EC2 instance](https://user-images.githubusercontent.com/97810379/151066223-4ddae4fd-f73e-4acb-86fb-78ffd4487492.JPG)

The EC2 instance I created was an AMI instance whose root user is "ec2-user" while I was using "ubuntu' - Solution link: https://stackoverflow.com/questions/33991816/ec2-ssh-permission-denied-publickey-gssapi-keyex-gssapi-with-mic

![Solution](https://user-images.githubusercontent.com/97810379/151066925-d6cbe394-1ba9-41c5-bc9e-a71dd05916a5.JPG)

Terminated the newly created AMI instance and relaunched a new ubuntu 20.04 instance => Successful

Connection to the new instance via GitBash successful

Tried installing NGINX on the new EC2 instance => Successful

Confirmed the NGINX service is running => active (running)

Opened TCP port 80 => Successful

Attempted to access the server locally in the Ubuntu shell, run: curl http://localhost:80 => Successful

Attempted to render the server on a web browser => Successful

## 2. INSTALLING MYSQL
Installed MySQL server successfully

Confirmed MySQL server is running => Successful

## 3. INSTALLING PHP
Installed PHP module that allows PHP to communicate with MySQL-based databases => Successful

Installed PHP fastCGI process manager => Successful

## 4. CONFIGURING NGINX TO USE PHP PROCESSOR
Created the root web directory for projectLEMP => Successful

Assigned ownership of the directory with the $USER environment variable => Successful

Created a new configuration file in Nginx’s sites-available directory using Nano => Successful

Activate your configuration by linking to the config file from Nginx’s sites-enabled directory => Successful

Tested the configuration for syntax errors => No errors found

Disabled the default Nginx host that is currently configured to listen on port 80 => Successful

Created an index.html file in the projectLEMP location => Successful

Opened your website URL using IP address and (public hostname) DNS name => Successful

## 5. TESTING PHP WITH NGINX
Created a test PHP file in the document root named info.php => Successful

Accessed the page in the web browser by visiting the domain name or public IP address => Successful

Removed the info.php file => Successful

## 6. RETRIEVING DATA FROM MYSQL DATABASE WITH PHP
Created a database - Test_DB => Successful

Created a new user - Test_User - and set up the user password => Successful

Gave Test_User permission over Test_DB => Successful

Created a table - todo_list - on the Test_DB => Successful

Inserted a few rows of content in table Test_DB.todo_list => Successful

Created a new PHP file - todo_list.php - in the custom web root directory using Nano => Successful

Accessed the page in the web browser by visiting the domain name followed by todo_list.php => Successful
![todo_list_php_page](https://user-images.githubusercontent.com/97810379/151440047-890186bb-d239-4877-8c4f-bea598a6ee10.JPG)
