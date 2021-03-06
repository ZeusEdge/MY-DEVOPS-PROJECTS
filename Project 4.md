# MEAN STACK DEPLOYMENT TO UBUNTU IN AWS
Created a new EC2 Instance of t2.nano family with Ubuntu Server 20.04 LTS (HVM) image => Successful

![2022-02-20 14_13_16-Instances _ EC2 Management Console](https://user-images.githubusercontent.com/97810379/154844347-f72bf1a3-a641-436f-ad1a-55ef9d683dd8.jpg)

## Implementing a Simple Book Register Web Form Using MEAN stack
**Step 1: Installing Node.js**

Update ubuntu =>= _sudo apt update_

![2022-02-20 13_09_37-ubuntu@ip-172-31-93-96_ ~](https://user-images.githubusercontent.com/97810379/154844453-d1f4a7b1-2796-4465-8a1f-29e58777617d.jpg)

Upgrade ubuntu =>= _sudo apt upgrade_

![2022-02-20 13_11_58-ubuntu@ip-172-31-93-96_ ~](https://user-images.githubusercontent.com/97810379/154844742-3ee57746-a01a-4b92-830f-8bf5b7bf2635.jpg)

Add certificates =>= _sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates_

_curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -_

![2022-02-20 13_18_05-ubuntu@ip-172-31-93-96_ ~](https://user-images.githubusercontent.com/97810379/154844783-4b5ba8c9-20f8-4b7b-9a44-98a733387b67.jpg)

Install NodeJS =>= _sudo apt install -y nodejs_

![2022-02-20 13_19_17-ubuntu@ip-172-31-93-96_ ~](https://user-images.githubusercontent.com/97810379/154844851-6f9c8bce-18ed-4af8-bf50-311198b14d85.jpg)

Install npm – Node package manager =>= _sudo apt install -y npm_

Verified the versions of Node.js and npm that were installed.

![2022-02-20 14_30_20-ubuntu@ip-172-31-93-96_ ~](https://user-images.githubusercontent.com/97810379/154845017-a367746b-b72d-4db7-8f04-5bb4aa225a82.jpg)

Node.js installed successfully

**Step 2: Installing MongoDB**

_sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6_

_echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list_

Install MongoDB =>= _sudo apt install -y mongodb_

![2022-02-20 13_23_25-ubuntu@ip-172-31-93-96_ ~](https://user-images.githubusercontent.com/97810379/154845251-01a1748f-32ac-4208-9546-7b52de95ab0c.jpg)

Start The server =>= _sudo service mongodb start_

Verify that the service is up and running =>= _sudo systemctl status mongodb_

Install body-parser package =>= _sudo npm install body-parser_

The ‘body-parser’ package is needed to help process JSON files passed in requests to the server.

![2022-02-20 13_47_14-ubuntu@ip-172-31-93-96_ ~_Books](https://user-images.githubusercontent.com/97810379/154845343-5cfb6b94-679f-49e0-ba33-c2b4b1ff3d3b.jpg)

MongoDB installed successfully

Created a folder named ‘Books’. In the Books directory, initialized npm project =>= _npm init_

Added a file to the Books directory named server.js

Added the following code segment into server.js

[server.js.txt](https://github.com/ZeusEdge/MY-DEVOPS-PROJECTS/files/8104105/server.js.txt)

## INSTALL EXPRESS AND SET UP ROUTES TO THE SERVER
**Step 3: Installing Express and set up routes to the server**

Express is needed to pass book information to and from our MongoDB database

Installing Express Mongoose package =>= _sudo npm install express mongoose_

![2022-02-20 13_49_18-ubuntu@ip-172-31-93-96_ ~_Books](https://user-images.githubusercontent.com/97810379/154847660-660f757a-b0d8-4f37-88e5-d97fcbd77f3b.jpg)

Express is successfully installed

In the ‘Books’ directory, created a folder named apps

Added a file to the apps directory named routes.js

Added the following code segment into routes.js

[routes.js.txt](https://github.com/ZeusEdge/MY-DEVOPS-PROJECTS/files/8104155/routes.js.txt)

In the ‘apps’ directory, created a folder named models

Added a file to the models directory named book.js

Added the following code segment into book.js

[book.js.txt](https://github.com/ZeusEdge/MY-DEVOPS-PROJECTS/files/8104162/book.js.txt)

**Step 4: Setting up AngularJS to access the created routes**

In this case, AngularJS is used to connect our web page with Express and perform actions on the book register

In the ‘Books’ directory, created a folder named public

Added a file to the public directory named script.js

Added the following code segment into script.js whioch is the controller configuration defined in which AngularJS is called up.

[script.js.txt](https://github.com/ZeusEdge/MY-DEVOPS-PROJECTS/files/8104170/script.js.txt)

![2022-02-20 14_04_55-ubuntu@ip-172-31-93-96_ ~_Books](https://user-images.githubusercontent.com/97810379/154847691-8701b27d-382c-43c7-ba59-241570fddd10.jpg)

Added a file to the public directory named index.html

Added the following code segment into index.html

[index.html.txt](https://github.com/ZeusEdge/MY-DEVOPS-PROJECTS/files/8104177/index.html.txt)

AngularJS is successfully configured.

Started the server =>= _node server.js_

Opened the TCP port 3300 in the AWS Web Console for the EC2 Instance

![2022-02-20 15_37_31-MINGW64__c_Users_1_Downloads_DevOps](https://user-images.githubusercontent.com/97810379/154847958-0eed09b6-21cc-4061-b648-0a8ab7eb8497.jpg)

Accessed the application on the web browser => Successful

Added a couple of book details in the relevant fields and changes were seen on the CLI as seen below

![2022-02-20 14_04_55-ubuntu@ip-172-31-93-96_ ~_Books](https://user-images.githubusercontent.com/97810379/154848154-05f06b3a-1821-4e23-9ee5-c9817a5a37aa.jpg)

Upon refreshing the application on the browser, the details were displayed as seen below;

![2022-02-20 15_39_05-34 205 159 93_3300](https://user-images.githubusercontent.com/97810379/154848104-36de81ef-ecff-4c12-bcec-a298f946b5b4.jpg)
