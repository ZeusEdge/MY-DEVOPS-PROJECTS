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

Attempted to access the server locally in the Ubuntu shell, run: curl http://localhost:80 => Successful

Attempted to render the server on a web browser => Output was from the Apache Server that was previously set up

Removed NGINX from the EC2 instance by running "sudo apt remove --purge nginx" and "sudo apt autoremove" => Successful

Created a new instance => SUccessful

Tried connecting to the EC2 instance with GitBash => Unsuccessful, Error Message: permission denied (publickey gssapi-keyex gssapi-with-mic). aws
