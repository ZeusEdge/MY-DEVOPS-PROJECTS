**1. WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS**

Set up AWS account => Successful

Set up EC2 instance => Successful

Connection to EC2 instance => Unsuccessful, Error regarding default security group that was selected while setting up the EC2 instance

Terminated the EC2 instance => Successful

Launched a new EC2 instance => Successful, Created a new security group with one permission

Connection to EC2 instance => Successful

**2. INSTALLING APACHE AND UPDATING THE FIREWALL**

Installed Apache Server => Successful

Confirmed the Apache Server running as a Service => Yes

Attempted to open the Apache Server url on a web browser => Unsuccessful

Added a rule to EC2 configuration to open inbound connection through port 80 by editing the Inbound Rules => Successful

Opened the Apache Server url on a web browser => Successful

**3. INSTALLING MYSQL**

Installed MySQL Server => Successful

Ran a security script to remove some insecure default settings and lock down access to your database system => Successful

Set the MySQL root user password => SUccessful

Confirmed logging in to the MySQL server => Yes

**4. INSTALLING PHP**

Installed PHP package, PHP module for communication with the MySQL-based databases, and a package to enable Apache to handle PHP files => Successful

Confirmed the installed PHP version => PHP 7.4.3

**5. CREATING A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE**

