
#MEAN STACK DEPLOYMENT TO UBUNTU IN AWS

i opened AWS account and created a virtual server with Ubuntu Server 20.04 LTS (HVM) image.

![s1 f](https://user-images.githubusercontent.com/94229949/170739547-d5a855ea-b5d0-4688-babd-e25378eb1980.png)

I updated Ubuntu using sudo apt update

![s1](https://user-images.githubusercontent.com/94229949/170739838-5fda056d-26b3-43f5-aba6-b7abd0f8b2cd.png)

Then upgraded Ubuntu using sudo apt upgrade

![s2](https://user-images.githubusercontent.com/94229949/170740079-d861c2ad-56e3-40e5-a3dd-08fb5ab98b0b.png)

node certificates using  sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates and curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

![s3](https://user-images.githubusercontent.com/94229949/170740555-ecfba62c-0a06-4602-ba8a-5fa978a8f81b.png)

curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

![s4 deb ](https://user-images.githubusercontent.com/94229949/170740859-ec94f1c6-b187-403b-8336-e2e930c894dd.png)

Installed  NodeJS using "sudo apt install -y nodejs"


![s8](https://user-images.githubusercontent.com/94229949/170741555-1b5bb1b7-c776-4aa4-ae46-d86fa5398a30.png)

For this application, we are adding book records to MongoDB that contain book name, isbn number, author, and number of pages.
mages/WebConsole.gif

sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6 , echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list and installed mongodb

![s6 install mangodb full](https://user-images.githubusercontent.com/94229949/170742368-fbabed30-f982-4b1a-aa8d-c60ccd69d804.png)

To start the server i used command "sudo service mongodb start"

![s7 start server](https://user-images.githubusercontent.com/94229949/170742568-651575a0-9624-4905-9498-653a309051a7.png)

To Start The server "sudo service mongodb start", I Verified the service is up and running using command "sudo systemctl status mongodb"

![s9](https://user-images.githubusercontent.com/94229949/170743191-3e332065-3ebe-491c-af60-98466a83264f.png)

Installed npm – Node package manager using sudo apt install -y npm

![s10](https://user-images.githubusercontent.com/94229949/170743690-73199cf7-00b3-47a0-8d6a-c009062e1f30.png)

I need ‘body-parser’ package to help us process JSON files passed in requests to the server using command "sudo npm install body-parser"

![s11](https://user-images.githubusercontent.com/94229949/170744010-c0a8b03a-7ec7-4fb0-a87e-de849b04ee26.png)

I created a directory called Books using "mkdir Books && cd Books" In the Books directory,i initialize npm project using  "npm init"

![s12](https://user-images.githubusercontent.com/94229949/170744591-491abf9d-5879-47d2-a2b7-b030ed0caaf8.png)

I created a file to it named server.js "vi server.js"and paste the web server code into the server.js file.

The Mongoose package  provides a straight-forward, schema-based solution to model the application data. I use Mongoose to establish a schema for the database to store data of the book register using sudo npm install express mongoose

![s13](https://user-images.githubusercontent.com/94229949/170747144-7e1ad936-11ca-40b4-8f8a-d08fa8404b15.png)

In ‘Books’ folder, I created a folder named apps using "mkdir apps && cd apps" then Created a file named routes.js then vi routes.js to  paste my code into routes.js

In the ‘apps’ folder,I created a folder named models using command mkdir models && cd models 

Created a file named book.js then "vi book.js" paste my code into ‘book.js’

I Changed the directory back up to Books using "cd .." then i Start the server by running command "node server.js"

The server is now up and running then connected it via port 3300

![s14](https://user-images.githubusercontent.com/94229949/170751803-d7ae80f9-d6a0-47f4-9c87-4821eff97cee.png)

