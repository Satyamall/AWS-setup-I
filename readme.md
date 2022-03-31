
For setup aws cloud:
 - click on services
 - click on compute
 - click on EC2
 - click on instances
 - click on Launch instances
 - Step 1: Choose an Amazon Machine Image (AMI)
 - after choose click on select (Like ubuntu click on select).

After the setup on aws cloud and download the key pair name 

Run in local system:
 - open git bash
 - create a folder with any name
 - copy the key pair download file inside it
 - move inside in folder.
 - ssh -i "key pair file name" ubuntu@"paste the Public IPv4 DNS here" like this (ssh -i developers.pem ubuntu@ec2-43-204-22-52.ap-south-1.compute.amazonaws.com)
 - sudo apt-get update
 - sudo apt-get install apache2
 - cd /var/www/html
 - pico index.html
 - sudo rm index.html
 - sudo touch index.html
 - sudo pico index.html
-  ```js
 <html>
<body>
<h1>My first website!</h1>
</body>
</html>
 ``` 
 - ctrl + s
 - ctrl + o
 - ctrl + L
 - ctrl + x
- refresh the Public IPv4 address in browser.

For Node:
 ```js
 curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

 cd

 sudo apt-get install -y nodejs

// for check
 node 
 node -v
 ```

 for node work:

 ```js
 mkdir src

 cd src/

 npm init -y

 npm i express --save

 ls

// create index.js file
 touch index.js

 nano or pico index.js
 // write code in express

 pico package.json
 // set up start in script

 npm start

 // Public IPv4 address:3000 run in browser
 
 cd 

 killall -9 node

 cd src/

 sudo npm install pm2 -g

 pm2 start index.js

 pm2 monit
 ```
